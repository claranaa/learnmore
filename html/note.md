### meta视口标签

meta标签是HTML中head区的一个辅助性标签，它位于HTML文档头部的head标签和title标签之间，用来提供用户不可见的信息。

标准视口标签的设置：视口宽度和设备保持一致、视口的默认缩放比例1.0、不允许用户自行缩放、最大允许的缩放比例1.0、最小允许的缩放比例1.0

```html
 <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">

```



<meta name="viewport" content="width=device-width, initial-scale=1"> 
表示支持响应式设计；支持正常的绘制和缩放。

### HTML5存储方式

html5中的Web Storage包括了两种存储方式：sessionStorage和localStorage。

sessionStorage：用于本地存储一个会话（session）中的数据，这些数据只有在同一个会话中的页面才能访问并且当会话结束后数据也随之销毁。因此sessionStorage不是一种持久化的本地存储，仅仅是会话级别的存储。

localStorage：用于持久化的本地存储，除非主动删除数据，否则数据是永远不会过期的。

它们的用法是(key,value)或只有key

```
sessionStorage.setItem(“键名”,”键值”);
```