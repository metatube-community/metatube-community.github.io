# Sever deployment (后端部署)

## 写在前面

为了方便大多数人使用，插件后端在设计时尽量做到了简单并且即开即用，但是部署过程可能依然需要花费几分钟的时间，所以需要耐心往下看。（或者直接使用[**免费后端**](./free-servers.md)）

## 后端项目

后端项目名为`metatube-server`

二进制文件发布于：

- [GitHub Releases](https://github.com/metatube-community/metatube-server-releases/releases)

Docker 镜像发布于：

- [GitHub Container Registry](https://github.com/metatube-community/metatube-sdk-go/pkgs/container/metatube-server)

> 由于 DockerHub 的下载限制，建议优先选择 GitHub Container Registry 下载镜像。

## 如何部署

> `metatube-server`资源占用非常低，理论上任何内存>=128MB，硬盘>=2G 的机器，都可以直接运行二进制程序或者 docker 容器。

### 直接部署(★☆☆)

1. 从[Releases](https://github.com/metatube-community/metatube-server-releases/releases)下载最新后端程序。
2. 使用如下**任意模式**命令运行后端：

- 内存模式：`./metatube-server`
- 数据库模式(推荐)：`./metatube-server -dsn metatube.db`

> Tips：
>
> - 带`-v3`后缀的版本理论上运行效率更高，但是需要新版的 CPU 支持。
> - Windows 下可以直接双击运行，但是仍旧建议使用数据库模式持久化数据。
> - 默认端口为 8080，若出现端口占用的情况，可以使用`-port`参数配置其他端口。
> - Linux 下后台运行后端服务可以使用`nohup`、`systemd`、`Docker`等。
> - Windwos 下后台运行后端服务可以使用[`NSSM`](https://nssm.cc/)。

### Docker 部署(★★☆)

> 请确保部署平台已有 Docker 环境，否则请先安装[Docker](https://docs.docker.com/get-docker/)

直接运行以下任意一条命令即可：

- 内存模式：

```sh
docker run -d -p 8080:8080 --name metatube ghcr.io/metatube-community/metatube-server:latest
```

- 数据库模式(推荐)：

```sh
docker run -d -p 8080:8080 -v $PWD/config:/config --name metatube ghcr.io/metatube-community/metatube-server:latest -dsn /config/metatube.db
```

更新后端需要先运行以下命令再重新跑一遍上述命令，**初次安装请跳过**

```sh
docker stop metatube
docker rm metatube
```

### Docker-Compose 部署(★★☆)

> 请确保部署平台已有 Docker、Docker-compose 环境

```sh
mkdir metatube-sdk-go && cd metatube-sdk-go
curl -sL https://raw.githubusercontent.com/metatube-community/metatube-sdk-go/main/docker-compose.yml -o docker-compose.yml
docker-compose up -d
```

### Raspberry Pi 部署(★★☆)

~~都用树莓派了，跑个 Docker 应该不需要教程吧~~

### Unraid 部署(★★☆)

参考：[Unraid 快速部署](../deploy/unraid/README.md)

### Synology 部署(★★☆)

参考：[这篇教程](https://www.baozhiqiang.xyz/index.php/archives/32/)

### Heroku 部署(★★☆)

‼️ Heroku 不再免费，请转至其他部署方式（如：Koyeb）

**优势：**

- ~~免费 🆓~~、速度快 ⚡️、简单部署+搭建不超过三分钟 ⏱。
- 不需要给后端配置代理，且使用美国 IP，刮削限制少。
- 自动支持 HTTPS，可以避免如 Emby 下图片加载的问题。

参考：[Heroku 一键部署](../deploy/heroku/README.md)

### Koyeb 部署(★★☆)

**优势：**

- 永久免费 🆓（只要不倒闭）。
- 自动支持 HTTPS。

参考：[Koyeb 快速部署](../deploy/koyeb/README.md)

### Mogenius 部署(★★☆)

**优势：**

- 免费 🆓。
- 自动支持 HTTPS。

参考：[Mogenius 快速部署](../deploy/mogenius/README.md)

## 参数配置

| **参数名**        | **可选值**   | **默认值** | **备注**                                         |
| ----------------- | ------------ | ---------- | ------------------------------------------------ |
| PORT              | int<0-65535> | 8080       | 监听端口号，按需修改                             |
| TOKEN             | string       | _无_       | 访问密钥，按需配置，若部署在本地则没有配置的必要 |
| DSN               | string       | _内存模式_ | 数据库服务地址，按需配置，小白建议使用默认值     |
| DB_MAX_IDLE_CONNS | int          | 0          | 最大空闲数据库连接数，建议使用默认值             |
| DB_MAX_OPEN_CONNS | int          | 0          | 最大数据库连接数，建议使用默认值                 |
| DB_PREPARED_STMT  | bool         | false      | Prepared Statement，建议使用默认值               |
| DB_AUTO_MIGRATE   | bool         | false      | 数据库表自动迁移，建议使用默认值                 |
| REQUEST_TIMEOUT   | string       | 1m         | 请求超时时长，默认一分钟                         |

### 关于`DSN`

- SQLite
  - 当传入的是文件名（如`library.db`）等字符串时，则会使用 sqlite 作为数据库引擎。
  - 默认使用`file::memory:?cache=shared`为参数的 sqlite 内存模式，但是数据非永久。
- PostgresSQL
  - 如果传入的是`^postgres(ql)?://`开头的链接，则会使用 postgres 作为数据库引擎。

> DSN 留空服务端则会默认使用 sqlite 内存模式，这当然是最简单的使用方式。但是如果关闭服务端，那么之前**服务端**爬取以及保存的所有数据也都会消失。（Jellyfin/Emby 已经刮削的数据当然不会消失）
>
> 配置 DSN 在一定程度上可以加快刮削速度，提升使用体验，**建议有一定动手能力的用户使用**。

### 关于`DB_AUTO_MIGRATE`

该选项会自动创建数据表，**第一次使用时需要开启**。
