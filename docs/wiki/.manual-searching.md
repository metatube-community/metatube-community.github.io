# Manual searching (手动识别)

## 如何手动识别

有些时候会存在因为搜索、命名等各类原因导致无法正确自动识别出影片的情况，此时就需要手动搜索。

### 常规搜索

直接在 `识别`>`标题` 中输入想要搜索的影片**番号**即可，如：

- `IPX-230`
- `ABP-330`
- `HEYZO-1234`

### 常规搜索+源匹配

在常规搜索的基础上输入的同时，在 `MetaTubeId` 下输入需要使用搜索的源，如：

- `FANZA`
- `JavBus`

> 具体源支持查看此[页面](https://github.com/metatube-community/jellyfin-plugin-metatube/wiki/%E6%95%B0%E6%8D%AE%E6%9D%A5%E6%BA%90)。

### 精准ID搜索

直接在 `MetaTubeId` 下输入需要使用搜索的源+**ID**，如：

- `FANZA:ssis00120`
- `ARZON:145678`
- `JavBus:ABP-033`

> 注意：ID不是番号，是每个影片网页地址固定的格式ID。

### 精准URL搜索

直接在 `识别`>`标题` 中输入想要搜索的影片的源链接即可，如：

- `https://www.dmm.co.jp/digital/videoa/-/detail/=/cid=sivr00212/`
- `https://duga.jp/ppv/mousouzoku-8162/`
- `https://www.javbus.com/ja/SABA-775`
