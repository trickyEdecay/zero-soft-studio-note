# 响应式网页设计

创建的页面排版大小可以智能地根据用户行为以及使用的设备环境进行相对应的布局。





## 媒体(media)查询

* 使用 @media 查询，你可以针对不同的媒体类型定义不同的样式。


``` html
@media only screen and (max-width: XXXpx) {
    body {
        style
    }
}
```



***



* 添加断点

``` html
@media only screen and (max-width: 768px) {
    style {

		/* 手机样式 */

    }
}
```

``` html
@media only screen and (min-width: 768px) {
    style {

		/* 笔记本样式 */
	}
}
```



***



* 横屏/竖屏

``` html
@media only screen and (orientation: portrait/landscape) {
    style {
        /* 横屏竖屏 */
    }
}
```

