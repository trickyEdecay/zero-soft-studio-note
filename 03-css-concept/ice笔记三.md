# CSS笔记三

## 伪类选择器pseudo-class 

1. 注意顺序问题，link visited hover active建议按此顺序写代码。记忆方法：love hate
2. 伪类选择器可叠加，顺序不会影响其效果。但建议love hate 仍按此顺序。
3. 关于focus这个伪类，不是所有元素都能获得焦点。但可以修改成有，用tabindex=正整数（按顺序）
4. 选定指定位置的子元素  :nth-child(2n/2n+1)
5. 选定指定类型的子元素  :nth-of-type



## 盒子模型

1. 所有的元素都适用此模型

2. 行内元素不可以设置宽高。它设置margin，左右有效，上下无效；设置padding，上下左右都有效，即会撑大空间

3. margin会发生合并/折叠/塌陷，如相邻的兄弟块级元素，父元素和子元素（取大值）会产生此现象。

   若想取父元素的值，则设置边框border，告诉他不要超过此边界。

4. 行内块不等于块级元素，所以不是合并而是用叠加。若不设置margin，也会有间隙。换行符导致的空格。
    解决办法：
    --去换行符
    --设置大块字体大小为0；再在小块设置字体大小。font-size
    --.margin-left:-5px(负值)；

5. padding  上 顺时针。border-radius 左上 顺时针 

6. box-sizing:border-box;

   >`border-box` 告诉浏览器去理解你设置的边框和内边距的值是包含在width内的。
   >也就是说，如果你将一个元素的width设为100px,那么这100px会包含其它的border和padding，内容区的实际宽度会是width减去border +
   >padding的计算值。大多数情况下这使得我们更容易的去设定一个元素的宽高。





## 块元素和行内元素

1. 可通过修改display将行内元素修改成块元素，也可以将块元素设置成行内元素。
2. 行内元素脱离文档流后也会成为块元素，float。
3. margin:0 auto；块级元素居中。
4. 行内元素不能包含块元素，虽然能正常运行，但是不符合语法。
5. 想让行内元素居中，可以用块级元素包含。





## 可替代元素和不可替代元素

1. 当你看到源代码某些元素的时候，无法想象出页面布局是怎样的，这样的元素可以理解为可替代元素。
2. img，inline-block是可替代元素，但是当inline-block里面有内容的话它就变成了不可替代元素。
3. 行内元素不可以设置宽高。但行内元素的可替代元素的宽高由内在尺寸决定如img，input。不可替代元素的宽高由其文字内容之类的决定。





## 文档流和文本流

1. 文档流即正常流，normal-flow。从上到下从左到右。
2. 文本流，概括地说其实就是一系列字符，是文档的读取和输出顺序，也就是我们通常看到的由左到右、由上而下的读取和输出形式，在网页中每个元素都是按照这个顺序进行排序和显示的，而position属性可以将元素从文本流脱离出来显示。



## 基线

1. 行高指基线到基线的距离。line-height=div的高度。
2. 当参差不齐时，vertical-align:baseline/bottom/......;(都试试找到对齐的即可)
3. 设置当前元素和父元素的基线如何对齐 vertical-align。
4. 可替换元素的基线在最底部？



## 定位
1. position 的四个值：static、relative、absolute、fixed。
2.  绝对定位：absolute 和 fixed 统称为绝对定位
3. 相对定位：relative，**相对于原来位置移动，元素设置此属性之后仍然处在文档流中，不影响其他元素的布局**
4. 默认值：static



## 文字样式

1. font-family 设置文字字体

   > --衬线字体
   >
   > --非衬线字体

2. font-size 设置文字大小

3. font-weight:100-900设置文字粗体

4. font-style 设置文字斜体



## 转义字符

>  有需要请百度
>
> 

## 边界和溢出问题

  overflow: scroll/ visible/ **auto**/ **hidden**



## 开启bfc

1. block formatting context  块级格式化上下文

2. 开启bfc可解决高度塌陷问题

3. 如何开启bfc：

   --设置元素浮动  float:left/right

   --设置元素绝对定位   position:absolution/fixed

   --设置元素为inline-block

   --将元素的overflow设置为一个非visible的值  如overflow:hidden



