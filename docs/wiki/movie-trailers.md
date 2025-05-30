# Movie trailers (影片预告)

## 工作原理

MetaTube for Jellyfin/Emby 的预告功能基于[strm 文件](https://support.emby.media/support/solutions/articles/44001159147-strm-files)实现，此功能会在影片目录下生成一个`trailers`文件夹以及相应的`.strm`预告文件，文件大小通常不会超过 100 个字节，因为文件本身只包含一个预告链接，所以几乎不会占用本地空间容量。

由于 Jellyfin/Emby 自身实现原因，它们内置的在线预告仅支持播放 YouTube 的链接格式，但是由于 MetaTube 影片及其预告的特殊性，均不可能通过 YouTube 链接去支持。所以目前似乎没有比使用`.strm`文件更加优雅的方式来支持在线预告的功能。

> MetaTube for Plex 原生支持在线预告，仅需在设置中开启即可，以下内容仅针对 Jellyfin/Emby 插件。

## 使用方法

1. 在插件配置里勾选`Enable Trailers`选项。
2. 如果**之前已经刮削过**，请手动刷新元数据。
3. 进入计划任务，运行`Generate Trailers`任务。
4. 重新扫描一遍媒体库，即可生成可播放的预告文件。

> PS：除了前两步，其他均会由计划任务定时完成，一般无需手动操作。

## 注意事项

- ~~⚠️ 播放第一次刷新或扫描出的影片预告，会显示**不兼容的流**，这是正常的，需要完成使用方法中所有步骤才能正常播放。~~
- ⚠️ 必须**完整完成使用方法中所有步骤**预告功能才能正常工作，例如等待计划任务完成、媒体库扫描完毕等。
- ⚠️ 该功能几乎会在每个视频目录下**生成一个`trailers`文件夹**，介意的使用者请勿开启此功能。
- ⚠️ 请确保每个视频**单独**放一个文件夹，例如`XXXX-000/XXXX-000.mp4`，不然会导致预告无法匹配播放等问题。（分集 cd 后缀或多版本的视频放在同一个文件夹下不会影响该功能）
- 部分预告无法播放可能是代理问题，如 MGS 预告必须要日本或美国的 IP 才能播放。
- 部分使用 SOD 的源无法播放预告是由于 SOD 不支持直接通过 URL 访问其预告资源导致的。
- 刮削时尽量选择带有预告资源的刮削源，如 FANZA、MGS 等，而不是像 JavBus 这种。
- 由于 Jellyfin/Emby 的限制，目前只能通过计划任务的方式生成预告文件，然后扫描媒体库之后才能正常播放预告。
