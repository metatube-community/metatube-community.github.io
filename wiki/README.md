![Plugin Banner](/logos/banner.png)

<p align=center>Wiki of MetaTube Plugin</p>

## 快速开始

1. 部署后端

- ➤ 请看《[后端部署](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E5%90%8E%E7%AB%AF%E9%83%A8%E7%BD%B2)》页面。

2. 安装插件

- ➤ 请看《[插件安装](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E6%8F%92%E4%BB%B6%E5%AE%89%E8%A3%85)》页面。

3. 配置插件

- 进入 JavTube 插件所在的配置页面。
- 输入之前配置好的后端地址 URL 以及需要的后端密钥 Token。
- 进入需要使用插件的媒体库：
  - 务必选择`电影`作为媒体库类型。
  - 勾选`JavTube`作为元数据下载器与图片获取器。

4. 具体使用

- 在添加完视频后，点击`扫描媒体库`按钮。
- 使用`刷新元数据`以更新数据内容。
- 使用`识别`手动搜索影片或演员数据。

5. 插件更新

- 通过存储库 URL 添加的插件，Jellyfin会在后台自动更新。
- Emby 版本的 JavTube 插件会通过计划任务自动更新。

> PS：需要重启 Jellyfin/Emby 服务，插件才会生效。
>
> 其他例如自动翻译、人脸识别等配置，可以参考右侧页面的相关内容。

## 问题反馈

> 遇到问题前可以先查看[常见问题](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98)中是否已存在类似的问题。

- 如果你遇到任何的 BUG，欢迎来 [Issues](https://github.com/javtube/jellyfin-plugin-javtube/issues) 区提交。
- 如果你有任何其他的问题，可以来 [Discussions](https://github.com/javtube/jellyfin-plugin-javtube/discussions) 或加入 [TG群](https://t.me/JavTubePlugin) 讨论。

## 参与开发

如果你擅长`C#`或`Go`语言且希望一同开发维护本项目，可以加入TG群讨论。

## 授权许可

本插件项目在 [MIT](https://github.com/javtube/jellyfin-plugin-javtube/blob/main/LICENSE) 许可授权下发行。此外，如果使用本项目表明还额外接受以下条款：

- 本插件仅供学习以及技术交流使用
- 请勿在公共社交平台上宣传此项目
- 使用本软件时请遵守当地法律法规
- 法律及使用后果由使用者自己承担
- 禁止将本软件用于任何的商业用途
