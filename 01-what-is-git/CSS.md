[TOC]

# CSS

## 选择器

<a class:>

.button{

background:purple;

color:white;

border-radius: 5px;

text-align:center;

line-height: 40px;

}

.button: hover{ //==伪类选择器== pseudo-class}

.button:active{}

.button:hover(悬停){}

**伪类选择器的先后顺序：==l==o==v==e ==h====a==te**

a:link{}(当有链接时可修改a标签的字符)

a:visited{}

a:hover{}

a:active{}

.a{outline:none;}

.a focus{

border: lpx solid red

}

.b:margin:{}

```css
.container{
  display:inline-block;
  background:black;
  color:white;
  width:48px;
  heigh:48px;
  border-radius:48px;
  text-align:center;
  line-height:48px;
  margin:5px;
}
.container:hover{
  background:red;
} 
```

# HTML

`<input class="a" tabindex="b">`

```
<div class="a"></div>
```

<div class="a">
<p> 第一个子元素</p>  
<h1>第二个子元素</h1>
<span>第三个子元素</span>
<span>第四个元素</span></div>

.a h1: first-child{}(必须是父元素出现的第一个元素,若不是出现在第一行则失效)

.a h1: first-of-type{}(父元素的首次出现的h1标签)

li: nth-of-type(n){}

<ul>
    <li>萝卜</li>
    <li>青菜</li>
    <li>玉米</li>
    <li>火腿</li>
    <li>鱼</li>
</ul>

伪类选择器可以叠加：.a nth-of-type hover{}

<div class=container>1</div>
<div class=container>2</div>
<div class=container>3</div>
<div class=container>》</div>

# 盒子模型

1. contentarea

2. padding

3. border

4. margin

5. border-radius(圆角)

   *圆角的宽高设置成与盒子一致时等于圆形*

*注意：所有元素都适用于盒子模型*

行内元素不能设置padding-bottom，margin，块级元素则都可以

1. 相邻的兄弟块级元素之间会产生这种效果（外边距的塌陷/合并/折叠）

2. 父元素和子元素外边距重叠时取大者，而不是叠加

## 行内元素和块级元素的区别

1. 块级元素占满一行，行内元素则不会
2. 行内标签要包含在块级标签里，反之不能
3. 行内元素不能设置宽高

### 可替换元素

img标签（通过文字不可以想象到的）

### 不可替换元素

normal flow文档流（从上到下，从左到右）

`.a span{`

`display: inline-block(行内块)}`（无视1和3原则）

```html
<div class=containers></div>
```

去掉效果里面的空格：

1. 不要换行符

2. 设置font-size（字体大小）

3. 设置margin-left为负值

`vertical-align:baseline(默认值)/button/top/middle;`

*注意：每个元素有它默认的基线*

line height(行高): 基线到基线的距离

无设置时由系统自由分配：`margin-right:auto;`

上下边距不要，左右边距自由分配：`margin:0 auto;`

## 块级元素居中

1. 水平居中：`text-align:center;` `margin-right:auto;margin-left:auto;`/`margin:auto 0;`(一般用于网页的大框架里)
2. 竖直居中

