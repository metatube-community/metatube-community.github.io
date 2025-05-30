# Proxy configuration (代理配置)

## 建议

由于刮削源的特殊性，对于后端，使用者都需要有一个能够正常访问**真正互联网**的网络，且最好出口 IP 为**日本**或**美国**（因为部分刮削源仅对以上两个地区完全开放）。

所以，首选部署后端的方式为`Cloud-Native`方式，其次为部署在 VPS 上，再之后是部署在本地。

部署在本地最好有软/旁路由的全局上网环境，**实在不行**才需要考虑使用代理。

确实需要使用代理的接着往下看。

## 后端

`metatube-server`后端支持环境变量的方式使用代理，支持的代理类型为 HTTP 代理。目前大多数的科学上网工具都支持以 HTTP 代理接入上网的选项。

> 注意：本文默认使用者已经知道环境变量的基础概念，如果不清楚此概念可以先花 5 分钟谷歌一下。

环境变量即为简单的键值对，在 Linux 中配置环境变量：

```shell
export HTTP_PROXY="http://ip:port"
```

在 Docker 中配置环境变量：

```shell
docker run -e HTTP_PROXY="http://ip:port"
```

在 Docker-compose 中配置环境变量：

请看此[文档](https://docs.docker.com/compose/environment-variables/)。

~~考虑到后端基本通过`docker-compose`部署，可以查看后端部署页面的内容。~~

## 例子

假设用户使用配置的 HTTP 代理地址为`192.168.1.2:7890`，SOCKS 代理地址为`182.168.1.2:7891`。

只需要为后端配置以下两个环境变量即可使用代理：

**注意：必须要同时配置`HTTP_PROXY`和`HTTPS_PROXY`两个环境变量才能正常使用代理！**

### 使用 HTTP 代理

- `HTTP_PROXY=http://192.168.1.2:7890`
- `HTTPS_PROXY=http://192.168.1.2:7890`

### 使用 SOCKS5 代理

- `HTTP_PROXY=socks5://192.168.1.2:7891`
- `HTTPS_PROXY=socks5://192.168.1.2:7891`

> 对于插件本身而言，只要保证能正常访问后端即可。如果访问后端存在网络问题才需要配置代理，配置方式与后端相同。
