# Metadata providers (数据来源)

## 支持的刮削源

- <https://github.com/metatube-community/metatube-sdk-go/tree/main/provider>

> 注意：刮削源尽量遵守以官方数据源为主的原则，第三方提供源通常存在数据不准确或是数据缺失的问题。

## 启用的刮削源

可以在 `/v1/providers` 的 API endpoint 下查看所有后端开启的刮削源。

例如：

- http://METATUBE_SERVER/v1/providers

## 调整刮削源优先级

现在通过设置环境变量即可手动修改 MetaTube Server 的刮削源优先级。

例如：

### 新版（v1.4+）

- 将`AVBASE`的优先级设置为 1000：`export MT_MOVIE_PROVIDER_AVBASE__PRIORITY=1000`
- 将`GFriends`的优先级设置为 99：`export MT_ACTOR_PROVIDER_GFRIENDS__PRIORITY=99`
- 将`JavBus`从刮削源中移除（设置为 0）：`export MT_MOVIE_PROVIDER_JAVBUS__PRIORITY=0`

> ⚠️ 注意：Provider 名称和 `PRIORITY` 属性名之间是**双下划线** `__`.

### 旧版（v1.3-）

- 将`AVBASE`的优先级设置为 1000：`export MT_MOVIE_PROVIDER_PRIORITY_AVBASE=1000`
- 将`GFriends`的优先级设置为 99：`export MT_ACTOR_PROVIDER_PRIORITY_GFRIENDS=99`
- 将`ARZON`从刮削源中移除（设置为 0）：`export MT_MOVIE_PROVIDER_PRIORITY_ARZON=0`

> 注意：刮削源名称以及默认优先级请参考 [provider](https://github.com/metatube-community/metatube-sdk-go/tree/main/provider) 目录下的具体刮削源中的 `Name` 和 `Priority` 字段。
> 优先级通常应当设置在 `1000 ± 10` 范围以保证最佳刮削排序质量。
