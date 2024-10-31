# Plugin installation (插件安装)

## 安装之前

请先确保当前的 Jellyfin/Emby/Plex 为**最新的**稳定版本，因为作者开发精力有限且 Jellyfin/Emby/Plex 的测试版本存在诸多不稳定性，所以本插件现在不会日后也不会提前支持这两个平台的 beta 版本。

在 Jellyfin/Emby/Plex 的 beta 测试版本中出现的插件无法识别，插件无法使用等问题，请勿在 Issue 中提问，亦不做任何解答，望谅解。

## Jellyfin

1. 进入 Jellyfin 控制台 > 插件目录/存储库 > 设置，点击添加
2. 输入存储库名称：`MetaTube`
3. 输入存储库 URL：[`https://raw.githubusercontent.com/metatube-community/jellyfin-plugin-metatube/dist/manifest.json`](https://raw.githubusercontent.com/metatube-community/jellyfin-plugin-metatube/dist/manifest.json)
4. 在插件目录下找到 MetaTube，点击安装
5. 重启 Jellyfin

_适用于中国大陆的存储库 URL：[`https://cdn.jsdelivr.net/gh/metatube-community/jellyfin-plugin-metatube@dist/manifest.json`](https://cdn.jsdelivr.net/gh/metatube-community/jellyfin-plugin-metatube@dist/manifest.json)（可能有缓存）_

## Emby

1. 从 [Releases](https://github.com/metatube-community/jellyfin-plugin-metatube/releases) 下载 MetaTube 最新插件
2. 解压出 MetaTube.dll 文件
3. 将 dll 文件复制到 Emby 插件目录
4. 重启 Emby 服务

PS：Emby 后续插件更新由计划任务在后台自动完成。

## Plex

如何找到 Plex 插件目录请参考：<https://support.plex.tv/articles/201106098-how-do-i-find-the-plug-ins-folder/>

1. 从 [GitHub](https://github.com/metatube-community/metatube-plex-plugins/archive/refs/heads/main.zip) 或 [Releases](https://github.com/metatube-community/metatube-plex-plugins/releases) 下载最新的插件 zip 文件
2. 将解压后的 `MetaTube.bundle` 文件夹移入 Plex 插件目录的根目录
3. 其中文件夹 `MetaTubeHelper.bundle` 为辅助插件，可选择性安装
4. 重启 Plex 服务

## 目录

常见的 Emby 插件目录如下：

- 群晖
  > /volume1/Emby/plugins
- Windows
  > emby\programdata\plugins
- Docker
  > <配置文件夹>/plugins
- Linux（供参考）
  > /var/lib/emby-server/plugins/
