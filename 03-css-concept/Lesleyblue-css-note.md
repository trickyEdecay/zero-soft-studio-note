# CSS
## 伪类选择器（Pseudo-classes）
1. :link 是改变未访问的链接的样式
 ```css
 a:link{
  color:blue;
}
 ```
2. :visited是改变访问过的链接的样式 
```css
a:visited{
    color:red;
}
```
3. :hover 鼠标移动到链接上 
```css
a:hover{
    color:green;
}
```
4. :active 鼠标按下去不放手时链接的样式
```css
a:active{
    color:yellow;
}
```
注意：当我定义visited、link顺序时，显示的页面和正常情况没有区别
当我定义的顺序是a:visited、a:hover、a:link，这时会发现：把鼠标放到未访问过的蓝色链接上时，它并不变成绿色，只有放在已访问的红色链接上，链接才会变绿
***定义时，应该是link、visited、hover、active的顺序（LOVE hate）*** 

5. :focus 获得焦点(像input、a标签这种鼠标点击有效果的都可以获得焦点)
```css
input:focus{
    background:blue;
}
```
6. tabindex：在用tab键导航时，tabindex属性规定元素tab键控制次序，支持<a>、<button>、<input>标签
```html
<a href="https://www.baidu.com/" tabindex="2">百度</a>
<a href="http://www.google.com/" tabindex="1">Google</a>
<a href="https://home.firefoxchina.cn/" tabindex="3">火狐</a>
```

7. * :first-child
   * :first-of-type
   * :last-child
   * :last-of-type

8. li:nth-of-type(n):n可以是数字也可以是函数表达式
   可以改变表格的行的颜色方面阅读

   9.伪类选择器的叠加
## 盒子模型
1. ![盒子模型](https://i.loli.net/2019/04/19/5cb988e813c54.jpg)
2. height和width=content+border+padding
3. border有color、width、style三个主要属性
 >color是指定border的颜色
 >width是border粗细程度
 >style属性可以设置为none(不显示)、solid(实线)等等

4. padding:10px 20px 10px 10px 分别对应上、右、下、左(顺时针排序)，margin同理，padding：10px 5px是上下内边距是10px，左右边距是5px

5. 所有元素都适用于盒子模型

6. 外边距的合并：当两个盒子竖着并排时(垂直)，他们两个的外边距会合并，两个盒子的距离是其中外边距较大的那个。

   ![外边距合并](https://i.loli.net/2019/04/19/5cb99bc3aa8c1.png)
   ***只有普通文档流中块框的垂直外边距才会发生外边距合并。行内框、浮动框或绝对定位之间的外边距不会合并***

7. box-sizing:border-box  告诉浏览器去理解你设置的边框和内边距的值是包含在width内的。也就是说，如果你将一个元素的width设为100px,那么这100px会包含其它的border和padding，内容区的实际宽度会是width减去border +  padding的计算值。(content-box是默认值。如果你设置一个元素的宽为100px，那么这个元素的内容区会有100px宽，并且任何边框和内边距的宽度都会被增加到最后绘制出来的元素宽度中。)


## 可替换元素和不可替换元素
概念：替换元素是浏览器根据元素的标签和属性，来决定元素的具体显示内容，比如<img>,这些元素没有实际的内容；不可替换元素是内容直接呈现给浏览器，比如<p>、<h1>等等
可替换元素：根据标签类型和属性来显示
```html
<img src="baidu.jpg">  
```
不可替换元素：文字直接在浏览器显示
```html
<p> 这是段落的内容</p>
```
## 文档流
  从左到右、从上到下
## 行内元素和块级元素
1. 块级元素可以包含行内元素，反之则不可以
2. 行内元素要居中，就设在块级元素里面
3. 行内元素都是不可设置宽高的
4. 用属性display：inline-block可以把块级元素当做行内元素
5. 如果我在一个盒子里面放了两个行内块，当我把盒子的背景颜色设置成red,则行内块的下面或者上面和盒子之间会有一条缝隙，是基线（baseline）和下面（上面）的线的缝，怎么消除呢？
             不提倡用font-size：0的方法，通过在其中一个行内块设置vertical-align：bottom来消除
6. 行内块和行内块之间会产生一个空格，需要在父级元素添加font-size:0来消除空格
7. 一旦设置width，会自动补上margin-right
8. 让一个块级元素居中的方法：margin-left：auto、margin-right：auto或者是margin:0 auto
## 基线
   若两个盒子其中有一个不含文字，则会出现两个盒子一下一上的情况，这时候要在不包括文字的盒子里面添加一个属性vettical-align:bottom

## 布局
  ### position:这个属性是定义元素的定位类型，任何元素都可以定位
1. position:static(默认值)
2. position:absolute  脱离文档流，生成绝对定位的元素（忘记相对谁定位了？？）
3. position:relative  相对于原来位置移动，元素设置此属性之后仍然处在文档流中，不影响其他元素的布局
4. position:fixed  绝对定位，相对于浏览器窗口进行定位
5. 脱离文档流是指，这个标签脱了的文档流的管理，不受文档流的布局约束了，并且更重要的一点是，这个标签在原文档流中所占的空间也被清除掉了。 
6. 脱离文档流的定位机制有float:left(right)、position：absolute
7. float 属性定义元素在哪个方向浮动。以往这个属性总应用于图像，使文本围绕在图像周围
***假如在一行之上只有极少的空间可供浮动元素，那么这个元素会跳至下一行，这个过程会持续到某一行拥有足够的空间为止***
```html
<p>
<img class="a" src="https://i.loli.net/2019/04/20/5cba85ecebd0b.jpg">
这是第一段的文字
</p>
<p>这是第二段的文字</p>
<p>第三段的文字</p>
```
```css
.a{
  width:50px;
  height:50px;
  border:1px solid black;
  float:left;
}
```
![结果显示](https://i.loli.net/2019/04/20/5cba8812af8d0.png)

## BFC

1. 解决外边距塌陷的问题
2. 以下三种出现任意一种就不会出现父元素和子元素塌陷的情况
+ overflow
+ float
+ position
3. 触发BFC：
+ 设置除 float:none 以外的属性值（如：left | right）
+ 设置除 overflow: visible 以外的属性值（如： hidden | auto | scroll）
+ 设置 position 属性值为：absolute | fixed 
4. 当一个盒子内有很多文字时，用overflow:hidden 可以把超出的内容截掉（看不见）
5. overflow:scroll 有一个滚动条
6. overflow:visible  不处理溢出的部分
## 其他
1. 正文一般用14px或16px,t提示文字比正文小2个px
2. letter-spacing  字间距
3. word-spacing  字间距（只对英文生效）
4. font-family:字体
5. front-weight: 字体粗细 范围[100,900]，只能取整百

