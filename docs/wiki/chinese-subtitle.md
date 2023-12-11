# Chinese subtitle (中文字幕)

## 字幕标签

MetaTube 插件对于以下几种情况，会自动为影片添加`中文字幕`标签：

- 视频以`-C`或`-ch`后缀结尾，例如某堂下载的中字资源
- 视频目录下存在`.chi`，`.chs`，`.cht`，`.zh`，`.zh-cn`等结尾的字幕文件

例如：

- `XXX-yyy`
    - `XXX-yyy-C.mp4`
- `XXXX-yyy-C`
    - `XXXX-yyy_ch.mp4`
    - `XXXX-yyy-C.mp4`
- `XXX-yyy`
    - `XXX-yyy.mp4`
    - `XXX-yyy.chs.ass`
    - `XXX-yyy.chs.srt`

另外，这样的外挂字幕是**不被识别成中文字幕**的：

- `XXX-yyy.srt`
- `XXX-yyy.ass`

> **注意**：`中文字幕`标签需要在计划任务中运行`Organize Metadata`任务添加，该任务默认每天凌晨自动运行，需要马上添加的也可以手动运行。

## 字幕角标

在配置页面开启角标后，当影片存在内嵌字幕或者外挂字幕时，计划任务会给影片海报添加角标。

<!-- ![ssis-534](https://user-images.githubusercontent.com/28824352/188468123-a008409f-91b6-491e-b496-0abe9414f231.jpg) -->

自定义角标样式可以在配置页面中更改`Badge Url`成需要的图片链接，建议为`.PNG`格式。

使用内置默认样式的角标：`zimu.png`，留空会导致角标失效！

> **注意**：
>
> 1. 由于客户端存在缓存，所以有时候不会马上生效，可以尝试刷新或者清除浏览器缓存
> 2. `字幕角标`与`中文字幕`标签类似，也需要在计划任务中运行`Organize Metadata`任务添加
