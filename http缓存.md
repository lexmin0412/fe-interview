# Http 缓存

https://segmentfault.com/a/1190000015816331

第一步，发起请求

第二步，判断是否有缓存

第三步，判断缓存是否过期？使用 cache-control 和 Expires，先判断 cache-control 是否有 s-maxage/max-age 指令



Cache-control 指令：

- `no-store`不缓存

- no-cache 不使用本地缓存 ，需要使用协商缓存，也就是说先与服务器确定缓存是否可用。

