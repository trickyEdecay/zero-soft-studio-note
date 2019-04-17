# 响应式设计-----解决移动互联网浏览
关键特性：断点和媒体查询（具有跨浏览器的响应性和适配用户各种屏幕的能力）
# 如何设计
## 1. html中meta标签定义
      使用 viewport meta 标签在手机浏览器上控制布局
      <meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1" />
      通过快捷方式打开时全屏显示
      <meta name="apple-mobile-web-app-capable" content="yes" />
## 2.  Media Query（媒体查询）
     width会有min-width和max-width媒介查询可以被用在CSS中的@media和@import规则上，也可以被用在HTML和XML中。通过这个标签属性，我们可以很方便的在不同的设备下实现丰富的界面，特别是移动设备
### media query的语法
@media 设备类型  and（设备选取条件）
```css
/* 当浏览器的可视区域小于980px */
@media screen and ( max-width: 980px ) {
#wrap {width: 90%; margin:0 auto;
#footer {padding: 8% 5%;margin-bottom: 10px;}
}
```
```html
<link rel=“stylesheet” type=“text/css” media=“screen and （max-width： 480px），screen and （max-device-width： 480px）” href=“link.css”/>
```