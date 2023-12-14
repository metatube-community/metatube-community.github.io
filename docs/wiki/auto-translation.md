# Auto translation (自动翻译)

## 如何开启

自动翻译可以在插件配置中，**勾选相应的翻译模式（`Translation Mode`）开启**。

可选的模式组合：

- Disabled：禁用翻译
- Title：翻译标题
- Summary：翻译简介
- Reviews：翻译评论（仅 Plex）
- Title and Summary：翻译标题和简介
- Title, Summary and Reviews：全部翻译（仅 Plex）

> PS：选择需要的翻译引擎，百度翻译准确度高但是有一定的翻译限制，谷歌翻译速度快限制少但是准确性略低。部分翻译引擎需要提供对应的API密钥等。

## 选择语言

进入 `控制台` > `媒体库` > 选择需要翻译的媒体库 > `管理媒体库`，将首选下载语言设置为需要翻译成的语言，例如：`简体中文`。

> PS：开启翻译前刮削的所有影片依旧为原来的语言，如有需要可以手动刷新元数据更新。

## 翻译引擎参数（Plex）

在 Plex 中使用以下翻译引擎需要在`Translation engine parameters`配置中手动填入相关参数：

- **Google**: `google-api-key=XXX`
- **DeepL**: `deepl-api-key=XXX`
- **OpenAI**: `openai-api-key=XXX`
- **Baidu**: `baidu-app-id=XXX,baidu-app-key=XXX`

> `XXX`即为相关的参数值，参数之间使用逗号分隔。

如果需要特别指定 Plex 语言库中没有的语言，例如繁体中文/粤语等，可以参考翻译引擎支持的语言填写`to`参数，例如：

- **使用百度翻译需要的语言成粤语**: `baidu-app-id=XXX,baidu-app-key=XXX,to=yue`
- **使用百度翻译需要的语言成繁体中文**: `baidu-app-id=XXX,baidu-app-key=XXX,to=cht`

百度翻译语言支持列表参见：<https://api.fanyi.baidu.com/api/trans/product/apidoc#languageList>

其他的翻译引擎同理，请自行查阅相关文档。
