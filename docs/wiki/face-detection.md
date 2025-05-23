# Face detection (人脸识别)

**MetaTube** 与其他同类插件最大的区别在于完全无感知的人脸识别体验。

本插件人脸识别基于[pigo](https://github.com/esimov/pigo)项目在后端实现，无需任何配置，部署完后端即可使用。

**实现时有以下一些好处：**

- 完全离线识别
- 识别速度超快（低于 10 毫秒，通常只要<1ms 即可，远低于基于百度/谷歌 API 的在线识别耗时）

## 关于精度

其实这是一个伪命题，在提问精度之前我们需要知道为什么要人脸识别，因为需要基于人脸裁剪图像，仅此而已。

pigo 的精度略低于在线 API 的识别精度，但是 pigo 对于人脸大致位置的识别准确性很高（除了戴口罩之类的识别可能识别不出来），而且识别速度通常高于在线
API**两个数量级**以上，这对于快速的图像分发极其重要，而精度在这里没有任何意义。
