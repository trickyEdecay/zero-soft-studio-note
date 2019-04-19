# CSS重点
## 上：

#### 1. 伪类选择器（pseudo-class）：`:x`可以进行叠加

**注意顺序(LoVe HaAt)**

```
:link     没有访问过后的链接获得样式
:visited     链接访问过后获得样式
:hover     鼠标位于所在区域上获得样式
:active     鼠标点击获得样式
```
**高级选择器：**

```
x:first-child      x所在父元素的第一项须为x属性才能匹配该样式
x:first-of-type     x所在父元素出现的第一个x属性匹配该样式
x:last-child	  x所在父元素的最后项须为x属性才能匹配该样式
x:lastt-of-type     x所在父元素出现的最后一个x属性匹配该样式
x:nth-of-type(n)    匹配x的父元素下的所有x匹配该样式
```

li:nth-of-type(n)    匹配li父元素下的所有li

li:nth-of-type(2n+1)    匹配li父元素下的奇数项的li

li:nth-of-type(2n+1)    匹配li父元素下的奇数项的li
```css
li:nth-of-type(){  
    background:gray;
}
```

**:focus:获得焦点 **
```css
.a:focus {    //伪类选择器 pseudo-class
    
}
```
>tabIndex属性可以设置键盘中的TAB键在控件中的移动顺序,即焦点的顺序。



#### 2. 块级元素与行内元素：

**块级元素**

​	兄弟元素外边距塌陷，合并，折叠（取最大值）

​	父元素和子元素外边距也会合并（取最大值）

**行内元素不能设置宽高**

​	display:block;

​	display:inline-block;    (既能设置宽高，也能实现不独自占一行的功能)

>inline-block不会出现兄弟元素或者父子元素之间的边距合并

#### 3. Normal Flow 文档流（正常流）：

html的内容排列顺序从左到右，从上到下。



#### 4. 可替换元素：
**默认可替换元素的基线与其父级的基线重合**

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>baseline</title>
	<style>
		#out{
			background: #2888c4;
		}
		.in{
			display: inline-block;
			width: 50px;
			height: 50px;
			background:  #c4c4c4;
		}
		/*img{
			width: 50px;
			height: 50px;
		}*/
	</style>
</head>
<body>
	<div id="out">
		g
		<div class="in"></div>
        <div class="in"></div>
        /*<img src="">*/
	</div>
</body>
</html>
```
![replace](https://i.loli.net/2019/04/19/5cb9eb18ce170.png)

上图要实现内外盒子**一样高度**只需设置`vertical-align : ;` 即可

两个在里面的盒子**在写html时换行**导致中间有**默认空格**，相当于两个单词间的分隔，若要消除空格，**可在父元素中设置`font-size:0px;`盒子内容字体大小可通过font-size再进行设置**



## 下：

**一个标签可以有多个类名**

```css
.class{
	opacity:0.5;      /*0.0 （完全透明）到 1.0（完全不透明）*/
	outline:none;     /*去除点击后的边框*/
	overflow:hidden;   /*超出部分隐藏*/
    text-overflow:ellipisis;   /*应用于单行文本  溢出显示省略号*/
    white-space:nowrap;    /*当宽度不够时不换行*/
    					   /*pre 保留空格*/
	overflow:scroll;     /*出现滚动条*/
  						 /*overflow-y:auto; 自动处理*/	
	overflow:visible;   /*默认不处理*/
    letter-spacing:2px;   /*字体间距*/
    text-decoration:underline;  /*下划线*/
    							/*none 不修饰*/
}
```
**设置下面的样式父元素和子元素不会出现塌陷**

```css
.class{
    overflow:hidden;
    float:left/right;
    position:absolute/fixed;    /*fixed表示不会随着滚动条滚动而改变布局*/
}
```



```css
body{
	min-width:720px;   /*当页面宽度小于720px时会出现横向滚动条*/
}
```
**弹性布局**

flex container
flex item     直属子元素

```css
flex container{
	display:flex;
	flex-direction:column;
    flex-direction:row;   /*默认*/
    flex-direction:row-reverse;  /*改变主轴方向*/
    flex-wrap:nowrap;	/*默认*/
    flex-wrap:wrap;    /*子元素超出宽度（高度）会换行*/
    flex-wrap:wrap-reverse;   /*改变交叉轴方向*/
    				   /*主轴与交叉轴垂直*/
    justify-content:center;   /*控制主轴上元素的排列方式为水平居中*/
                  /*flex-start：主轴的开始  flex-end：主轴的末端*/
    			  /*space-between：两端对齐*/
    align-items:center;  /*控制交叉轴上的排列方式为水平居中*/
    			  /*flex-start：交叉轴的开始  flex-end：交叉轴的末端*/
    			  /*默认：stretch：当子元素没设置高度时，自动拉伸*/
    align-content:center; /*多条主轴相对交叉轴*/
    			  /*flex-start：交叉轴的开始  flex-end：交叉轴的末端*/
    			  /*默认：stretch*/
}
```
```css
flex item{
    flex-grow:1;   /*默认为0； */
    flex-shrink:1;
    flex-basis:;   /*相当于宽度或者高度 */
    flex: 0 0 20%;
    /* flex-grow | flex-shrink | flex-basis*/
}
```
