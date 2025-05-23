# Image cropping (封面裁剪)

## 自动裁剪

大多数情况下，某些影片封面均会先进行人脸识别再进行裁剪，对使用者而言完全无感知。

## 手动裁剪

在自动裁剪失败或不准确时，我们可能需要使用手动裁剪封面。手动裁剪有以下两种方式。

### 手动导入(★☆☆)

在编辑图像时，可以选择手动导入图片。不过除非有特殊需求（例如自定义新的封面），不然不建议使用该方式更新封面。

### 手动定位(★★★)

MetaTube 支持另一种半自动半手动的图像裁剪方式，这种方式不需要自己裁剪图片并上传，可以省去部分麻烦，比较推荐。

手动定位方法如下：

#### 在`编辑元数据` => `外部 Ids` 下找到 `MetaTube Id`的值，并复制，如

- `Provider1:1234`

#### 手动判断该影片封面主要中心位置`pos`，如

- 需要裁剪左侧四分之一的封面，记`0.25`
- 需要裁剪中心的封面，记`0.5`
- 需要裁剪右侧四分之一的封面，记`0.75`
- 需要裁剪靠右的封面，记`1.0`

#### 选择该影片，点击识别，然后在`MetaTube Id`中输入之前复制的值，并用冒号连接`pos`值，如

- `Provider1:1234:0.75`

#### 点击确认，封面即可完成半手动裁剪更新

_注意：0 <= pos <= 1，表示裁剪中心位置与图片宽度的比值。_
