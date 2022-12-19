# 部署到 Koyeb

**永久免费方案：**

- 2 Apps
- 2 Services per App
- 100GB outbound bandwidth included
- 1 custom domain
- Access to Nano and Micro instances
- 512MB maximum total memory across all apps
- Access to one Koyeb region
- Community support

参考本教程快速将`MetaTube`后端免费部署至[`Koyeb`](https://www.koyeb.com/)云平台。

## 具体步骤

> 以下步骤需要有Koyeb账号，没有账号的可以先[注册](https://app.koyeb.com/auth/signup)。

### 部署应用

- 进入Koyeb仪表盘，点击`Create App`。

![create-app](images/create-app.png)

- 输入App名字，例如`metaube`，然后点击`Next`。

![name](images/name.png)

- 选择`Docker`，并在Docker image下输入：`docker.io/metaube/metatube-server:latest`。

![docker](images/docker.png)

- 下拉，首先点击`Add Environment Variable`添加环境变量，接着在Key处填入`TOKEN`，在Value处填入你自定义的密钥，用于后续插件配置。

![token](images/token.png)

- 继续拉到底部，`Region`地区选择`par`，在Service name里输入`metaube`，点击`Create service`，然后等待完成部署。

> 目前Koyeb只有巴黎地区可选，若后续有其他北美或者亚洲地区可用，建议更换至离日本较近的区域，如新加坡等。

![region](images/region.png)

- App状态变成如下图所示的`Healthy`即表示部署完成。下面的Public URL即为MetaTube后端的URL，连同之前的TOKEN一起复制粘贴到MetaTube插件页面即可完成配置。

![done](images/done.png)

### 更新应用

- 更新后端，直接点击`Redeploy`并等待重新部署完成即可。

![redeploy](images/redeploy.png)
