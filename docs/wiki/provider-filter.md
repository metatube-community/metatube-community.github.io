# Provider filter (刮削过滤)

## 过滤与排序

新版插件支持根据刮削源结果重新过滤与排序。在插件配置页面中配置`Movie provider filter`，例如：

<!-- ### 默认刮削顺序

- `FANZA,Caribbeancom,FC2,Pcolle,1Pondo,10musume,KIN8,C0930,H0930,H4610,MYWIFE,MGS,XXX-AV,Gcolle,Getchu,PACOPACOMAMA,MURAMURA,HeyDouga,HEYZO,CaribbeancomPR,PRESTIGE,SOD,AVE,DUGA,TOKYO-HOT,ARZON,AVWIKI,JavBus,JAV321,AIRAV`

### 过滤无码源

仅供参考，不建议这么做

- `FANZA,MYWIFE,MGS,Getchu,PRESTIGE,SOD,DUGA,ARZON,AVWIKI,JavBus,JAV321,AIRAV` -->

### 只开启三个源

优先顺序为 JavBus>Arzon>AVWIKI（仅供参考，不建议这么做）

- `JavBus,Arzon,AVBASE`

⚠️注意：

- 所有刮削源的名字可以在[数据来源](./provider-source.md)中找到。
- 刮削源名字大小写不敏感，但字母必须一一对应。
- 刮削源优先级从左到右递减，必须使用**逗号**隔开。
- 开启此功能后，凡不在过滤列表内的源均会被过滤掉。
- 如果它日后端加入了新的刮削源，需要补充进过滤列表中。

> 另外，默认顺序是反复测试后得到的最佳顺序，如果没有特殊需求请尽量不要开启此功能以免影响使用体验。
