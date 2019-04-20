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
  height:48px;
  border-radius:48px;
  text-align:center;
  line-height:48px;
  margin:5px;
}
.container:hover{
  background:red;
} 
```

### position属性 

#### position:static

属性默认值，对象遵循正常文档流，top/bottom/left/right/z-index没有作用。

#### position:relative

相对位置布局，可根据top/bottom/left/right参数相对于正常位置相对偏移。

```
position:relative;
left:20px;
top:20px;
```

#### position:absolute

生成绝对定位的元素，相对于static定位以外的第一个父元素进行定位。

#### position fixed

脱离文档流，相对浏览器窗口定位，固定fixed区域位置。z-index确定层叠关系。



与fixed一起使用，显示同级内容，跳出弹窗后底面加一层灰色——opacity(透明度):0.5；

当块级元素设置成float后，它本身会脱离文档流，变成行内元素，文档流不变，但会推开<u>文字流</u>，后面不需要加display:block——float:left/right; 

*注意：只有块级元素可以浮动（float）*

修改字体：`font-family：“字体英文名”`（如所找字体不存在，则在后面加默认值san-serif）

font-weight:[100,900](字体宽度)

letter-spacing(字体间距):20px

下划线：`text-decoration:underline;/border-buttom=1px solid`

无视框长，直接显示一行：`white-space:nowrap`

white-space:pre

转义字符：&lt(<) &gt(>)

serif(衬线字体)：有像上钩，收尾之类的字体修饰的一种字体

san-serif(无衬线字体)

原装电脑上至少有一种衬线字体或者一种无衬线字体

monospace(等宽字体):写代码的字体一般是等宽字体



### display属性

规定元素应该生成的框的类型。*注意：所有主流浏览器都支持display属性。*

默认值，inline元素会被显示为内联元素，前后没有换行符：`display:inline`

行内块元素inline-block：`display:inline-block`

block元素将显示为块级元素，前后带有换行符：`display:block`

`display:flex;`/* flex块级，inline-flex行内块 */

### 弹性布局 

<u>Flex</u>是<u>Flexible Box</u>的缩写，意为<u>弹性布局</u>，用来为盒状模型提供最大的灵活性。

使用flex需要有一个父容器（container），父容器中包括几个items。

利用Flex布局的元素：fiex-container(Flex容器，简称容器)，它的所有子元素自动成为容器成员：fiex-item（Flex项目，简称项目）。

###### fiex-direction

只能设置在fiex container上的：`fiex-direction:column;`(把横向排列改为竖向排列)

`fiex-direction:rov-reverse;`(改变横向主轴方向)

###### fiex-wrap

默认值nonewrap（不换行）,若设置成wrap,则换行：`fiex-wrap:wrap;`

`fiex-wrap:wrap-reverse;`

*交叉轴会根据排列方向的改变而改变*

###### align-items

设定子元素在垂直交叉轴上的对齐形式。

交叉轴上元素的排列方式：`align-item:center;/align-item:flex-start;/align-item:flex-end;`

align-items:stretch;(默认值)

align-items:baseline;

###### align-content

定义了多根轴线的对齐方式。

align-content:flex-start;(与交叉轴的起点对齐)

align-content:center;(与交叉轴的中点对齐)

###### flex-basis(一个元素在主轴上的尺寸)

定义了在分配多余空间之前，项目占据的主轴空间（main size）。

###### flex-shrink

定义项目的缩小比例，默认为1：`flex-shrink:<number>;`

###### flex-grow

定义项目的放大比例：`flex-grow:<number>;`

不需要按需分配，不要长大和缩小：`flex-grow:0;`(默认值)

`flex:0 1 40px;(flex:flex-grow flex-shrink flex-basis的简写)`

###### justify-content(控制主轴上元素的对齐方式)

justify-content:center;(居中对齐)

justify-content:flex-start;(顶部对齐)

justify-content:flex-end;(底部对齐)

justify-content:space-between;(自动分配填补空间)

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

1. content：内容

2. padding：填充

3. border：边框

4. margin：边界

5. border-radius(圆角)

   *圆角的宽高设置成与盒子一致时等于圆形*

*注意：所有元素都适用于盒子模型*

行内元素不能设置padding-bottom，margin，块级元素则都可以

1. 相邻的兄弟块级元素之间会产生这种效果（外边距的塌陷/合并/折叠）
2. 父元素和子元素外边距重叠时取大者，而不是叠加

### 一个宽高均为200px的父元素，包含一个宽高均为100%的子元素

1. 父元素的<u>可分配空间</u>：就是在一个盒子模型里它的content-align大小;



父元素和子元素之间不会发生塌陷的三种情况：

#### 父元素和子元素之间不会发生塌陷的三种情况：

`overflow:hidden;`、`float:left/right`、`position:absolute/fixed`

#### 外边距塌陷的情况：

1. float的外边距不会塌陷；

2. inline-block的外边距会塌陷；

3. 产生了bfc,不会影响外面的元素块：`overflow:hidden;`

   overflow:visible;——与overflow:hidden;用处相反

溢出的文本显示省略：`text-overflow:ellipsis;`

### 行内元素和块级元素的区别

1. 块级元素占满一行，行内元素则不会
2. 行内标签要包含在块级标签里，反之不能
3. 行内元素不能设置宽高

### 可替换元素

img标签（通过文字不可以想象到的）

### 不可替换元素

normal flow：文档流（从上到下，从左到右）

`.a span{`

`display: inline-block(行内块)}`（无视1和3原则）

```html
<div class=containers></div>
```

去掉效果里面的空格：

1. 不要换行符

2. 设置font-size（字体大小）

3. 设置margin-left为负值

   *注意：编辑浏览器时，最小字体不要小于12px。*

`vertical-align:baseline(默认值)/button/top/middle;`

*注意：每个元素有它默认的基线*

line height(行高): 基线到基线的距离

无设置时由系统自由分配：`margin-right:auto;`

上下边距不要，左右边距自由分配：`margin:0 auto;`

#### 块级元素居中

1. 水平居中：`text-align:center;` `margin-right:auto;margin-left:auto;`/`margin:auto 0;`(一般用于网页的大框架里)

2. 竖直居中

   

scroll：滚动条

开发者工具：按F12或者按ctrl+shift+I或者鼠标右键弹出的菜单中选检查

calc()用在流体布局上，可以借此计算得到元素的宽度。

`width:calc[20%-20px];`（会消耗较多的浏览器资源，不建议常用）



