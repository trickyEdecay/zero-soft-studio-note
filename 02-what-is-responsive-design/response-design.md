# 全响应式设计

***

## 粗略理解

> 就是让一个页面在不同尺寸设备上自适应的显示出最佳排版
>
> ***
>
> 
>
> ## 官方定义
>
> **百度百科：**  
>
> 简而言之，就是一个网站能够兼容多个终端——而不是为每个终端做一个特定的版本。这个[概念](https://baike.baidu.com/item/%E6%A6%82%E5%BF%B5/829047)是为解决移动互联网浏览而诞生的。
>
> **未知名博客：**页面的设计和开发应当根据用户行为以及设备环境（系统平台、屏幕尺寸、屏幕定向等）进行相应的响应和调整。具体的实践方式由多方面组成，包括弹性网格和布局、图片、css media query的使用等。无论用户正在使用笔记本还是iPad，我们的页面都应该能够自动切换分辨率、图片尺寸及相关脚本功能等，以适应不同设备；换句话说，页面应该有能力去自动响应用户的设备环境。
>
> 响应式网页设计就是一个网站能够兼容多个终端——而不是为每个终端做一个特定的版本。这样，我们就可以不必为不断到来的新设备做专门的版本设计和开发了。
>
> 响应式设计的基本原理是通过媒体查询检测不同的设备屏幕尺寸做处理。页面头部必须有meta声明viewport：
>
> <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no”>
>
> ***
>
> ##  优缺点

**优：**灵活性强，快捷解决显示问题

**缺：**代码量大，效率低

***

## 实现工具

**媒介查询** - Media Query

****

###  关于media

**它能够获取：**

设备的宽和高device-width，device-height显示屏幕/触觉设备。

渲染窗口的宽和高width，height显示屏幕/触觉设备。

设备的手持方向，横向还是竖向orientation（portrait|lanscape）和打印机等。

画面比例aspect-ratio点阵打印机等。

设备比例device-aspect-ratio-点阵打印机等。

对象颜色或颜色列表color，color-index显示屏幕。

设备的分辨率resolution。



响应式布局、响应式html和css、响应式媒体、响应式javascript

***

##  响应式布局
一.设置meta标签
>在完成非响应式布局后，head中添加如下代码。设置meta标签，让视口宽度等于设备宽度，而且需要禁止用户缩放行为。
```html
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
<meta name="HandheldFriendly" content="true">
```
>这里视口的设置需要注意的是，视口就是可见的屏幕尺寸；设置视口时只设置宽度，而不在乎高度，这是因为高度由内容自动撑开。

二.媒体查询设置样式
>媒体查询（media query）是响应式设计的核心，它能够和浏览器进行沟通，告诉浏览器页面如何呈现。媒体查询，它查询的就是视口宽度，查询用户使用什么样的设备来访问的页面，知道了设备尺寸就可以调用相应的响应式代码。
>
>***
### 方式
**1.style标签中的media属性  **
根据屏幕宽度不同设置不同颜色

...

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>响应式布局</title>
    <style>
        body{
            margin: 0;
        }
    </style>

    <style media="screen and (max-width:340px)">
        body{  background: red; }
    </style>
    
    <style media="screen and (min-width:340px) and (max-width:720px)">
        body{  background: blue; }
    </style>　　　　　
</head>

...

**2.在link标签中设置media属性  ** 
通过引入外部css，也可以实现上面代码显示的效果。

<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>响应式布局</title>
    <link rel="stylesheet" href="720-1080.css" media="screen and (min-width:340px) and (max-width:720px)">   
</head>  
还要在.css中添加body{ background: blue; } 

**3.外链css样式中的@media属性**

```html
@media screen and (min-width:340px) and (max-width:720px) {
	body{
		background: blue;
	}
}
```

***

## 注意

IE6~8无法实现响应式媒体查询
解决方案：css3-mediaqueries.js。引入此文件可以解决IE6-8无法实现响应式媒体查询的尴尬。

