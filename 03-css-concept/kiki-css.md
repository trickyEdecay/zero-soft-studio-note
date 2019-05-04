# css
```
css由两个主要的部分构成：选择器，以及一条或多条声明
每条声明由一个属性和一个值组成
```
### 选择器
1.id选择器
```
<h2 id="special"></h2>
<head>
  <style>
     #special{
         color: blue;
             }
```
2.类别选择器
```
<h2 class="special"></h2>
<head>
  <style>
     .special{
         color: blue;
             }
```
3.标签选择器
```
p{
    color: red;
}
```
4.后带选择器
```
h1 span{
    color: red;
}
//改变span里字的颜色
```
5.子选择器
```
h1>span{
    
}
```
```
<h1>git<span>指令</span><span>someting</span?|></h1>
```
```
优先级：外部样式表的优先级<style标签<内联样式；
        标签选择器<类别选择器<id选择器
```
### 值的不同写法
```
颜色的表示方式除了可以用英文单词red，还可以用十六进制#ff0000: p{color: #ff0000;}，还可缩写为p{color: #f00;}
```
### 基本语法
```
css声明总是以分号结束，声明组以大括号括起来
```
```
1.<h1 style="text-align: center; color: red;background color: blue;">
```
```
2.注释：/*这是个注释*/
```
```
3.引入外部的css
<link href="css/main.css" rel="stylesheet">
//link用的是href,而不是src，rel标签属性不能省略
```
```
4.（1）.a h1: first-child{}  /*匹配父元素第一项的h1标签*/
（2）.a h1: last-child{}  /*匹配父元素最后一项的h1标签*/
（3）.a h1: first-of-type{}  /*匹配在父元素出现第一次的h1标签*/
```
```
5.行高是基线到基线的距离
```
```
6.可替换元素：img 宽高由本身宽高决定；
  不可替换元素：宽高由内容多少决定
```
```
7.取消基线：vertical-align: baseline
  对齐：vertical-align: botton;
  水平居中：text-align: center;
  垂直居中：line-height: center;
  自动填满一行：margin-right: auto;
  inline-block用于行内元素居中对齐
  圆标：iconfont
```
```
8.文档流：按从上到下，从左到右排列
```
```
9.position: static;/*默认值*/
  position: relative;/*相对位置，基于原来位置变化*/
  position: fixed;/*绝对定位，不会随滚动条的滑动而移动*/
  position: absolute;/*绝对定位,使其脱离文档流*/
```
```
10.display: inline-block;/*行内块*/
```
```
11.white-space: nowrap;/*不换行*/
   white-space: pre;/*多空格*/
```
```
12.转义
   &nbsp;代替一个空格
   &gt;代替大括号
   &lt;代替小括号
```
```
13.网页
（1）溢出 overflow: scroll/*出现滚动条*/
（2）宽容 overflow-y: scroll;/*出现竖向滚动条*/
         overflow-y: auto;/*自动决定是否出现滚动条*/
```
### 块级元素和内联元素/行内元素
```
每个标签都有自己默认的行为，自己会独占一行的标签元素叫做块级元素，，不会自己独占一行的标签元素叫内联元素/行内元素。
块级元素：p h1-h6 ul ol table div form
行内元素：img a input button label textarea select
两者区别：块级元素能够设计宽高，行内元素不行。
```
### 盒子模型
```
1.内边距
padding:10px 10px 5px 5px(上，右，下，左)
padding:10px 5px(上下，左右)
//0的话不要加单位px
2.外边距
margin:10px 10px 5px 5px(上，右，下，左)
margin:10px 5px(上下，左右)
3.外边距的合并/折叠/塌陷的两种情况（取较大值）
（1）相邻兄弟块级元素之间（同级）
（2）父元素和子元素
4.外边距不会出现塌陷
（1）两个元素设置绝对定位时，position:absolute/fixed;
（2）设置浮动时，float:left/right;
（3）inline: block; overflow:hidden;
```
### 按钮
```
<style>
   div{
       background: blue;
       color: #fff;
       border-radius: 5px;/*圆角*/
       text-align: center;
       box-sizing: border-box;
       width: 90px;
       height: 40px;
       line-height: 40px;
       cursor:pointer;/*光标移动到按钮时，会出现手指形状*/
   }
   .a: focus{
       border: 1px solid red;
   }/*获得焦点*/
   .button:hover{
       background: red;
   }/*悬浮*/
   .button:active{
       background: blue;
   }/*激活,设置按下颜色*/
   .a:link{
       color: red;
   }
   .a:visited{
       color: yellow;
   }
伪类选择器固有顺序：link,visited,hover,active
伪类选择器可叠加
```
# flex布局-弹性布局
### 1.定义
```
.box{
    display: flex;
}
行内元素也可使用弹性布局:
.box{
    display: inline-flex;
}
设为flex布局后，子元素的float、clear和vertical-align属性将失效。
```
### 2.基本概念
```
采用flex布局的元素，成为flex容器，它的所有子元素自动成为容器成员，称为flex项目，简称项目。
```
### 3.容器的属性
```
(1)flex-direction 决定主轴的方向，即项目的排列方向。
   ----- row:默认值，从左往右
   ----- row-reverse:从右往左
   ----- colum:从上往下
   -----colum-reversr:从下往上
```
```
(2)flex-wrap
  默认情况下，项目都排在一条线上。
  ---- nowrap:默认，不换行
  ---- wrap:换行，第一行在上方
  ----wrap-reverse:换行，第一行在下方
```
```
(3)flex-flow
是flex-direction属性和flex-wrap属性的简写，默认值为row nowrap
```
```
(4)justify-content
定义了项目在主轴上的对齐方式
---- flex-start:默认值，左对齐
---- flex-end:右对齐
---- center:居中
---- space-between:两端对齐，项目之间的间隔也相等
---- space-around:每个项目两侧的间隔相等，项目之间的间隔比项目的间隔大一倍
```
```
(4)align-items
定义项目在交叉轴上如何对齐
---- flex-start:交叉轴的起点对齐
---- flex-end:交叉轴的中点对齐
---- center:交叉轴的中点对齐
---- baseline:项目的第一行文字的基线对齐
---- stretch:默认值，如果项目未设置高度或设为auto,将沾满整个容器的高度
```
```
(5)align-content
定义多根轴线的对齐方式，如果项目中只有一根轴线，则该属性不起作用
---- flex-start:与交叉轴的起点对齐
---- flex-end:与交叉轴的终点对齐
---- center: 与交叉轴的中点对齐
---- space-between:与交叉轴两端对齐，轴线之间的间隔平均分布
---- space-around:每根轴线两侧的间隔相等。轴线之间的间隔比轴线与边框之间大一倍
```
### 4.项目的属性
```
(1)order
定义项目的排列顺序，数值越小，排列越靠前，默认为0
```
```
(2)flex-grow
定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大；若所有项目的flex-grow属性都为1，则他们将等分剩余空间；若一个项目的flex-grow属性为2，其他项目为1，则牵着占据的剩余空间比其他项目多一倍
```
```
(3)flex-shrink
定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小;如果所有项目的flex-shrink属性都为1，当空间不足时，都将等比例缩小。如果一个项目的flex-shrink属性为0，其他项目都为1，则空间不足时，前者不缩小
```
```
(4)flex-basis
定义了在分配多余空间之前，项目占据的主轴空间,浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小,它可以设为跟width或height属性一样的值，则项目将占据固定空间
```
```
(5)flex属性
是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto，该属性有两个快捷值：auto (1 1 auto) 和 none (0 0 auto)
```
```
(6)align-self
align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch，该属性可能取6个值，除了auto，其他都与align-items属性完全一致。
```


