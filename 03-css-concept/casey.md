# css的课后笔记

### `margin(外边距)`

```css
margin:0px 0px 0px 0px;上0px 右0px 下0px 左0px像素的外边距
margin:0px 0px 0px;指上 0px 左右 0px 下0px像素的外边距
margin:0px 0px; 指上下 0px 左右0px像素的外边距
margin 0px;   指上下左右各0px像素的外边距
外边距的合并问题 
如果是父子关系的块级元素合并问题可以在子元素那加个透明的border
如果是兄弟关系的块级元素合并问题可以在给元素开启BFC(块级格式上下文)
所谓BFC(块级结构上下文)就是盒子内随意变化 并不会影响到外面
开启这种结构的方式主要有
overfload:hidden；
float：left or right
position:absolute or fixed;
```



### `padding(内边距)`

```css
padding:0px 0px 0px 0px;上0px 右0px 下0px 左0px像素的内边距
padding:0px 0px 0px;指上 0px 左右 0px 下0px像素的内边距
padding:0px 0px; 指上下 0px 左右0px像素的内边距
padding 0px;   指上下左右各0px像素的内边距
具体用法和margin类似
但是行内元素是不支持左右内边距 但是支持上下外边距 虽然有实际效果 但是上下元素却感知不到
```

### `文本流(标准流)`

```
所谓文本流就是指浏览器在渲染html页面时 是按照从上到下 从左到右的顺序进行渲染 标签的排列格式也是按照这种顺序 那么这种顺序就叫做文本流
```

### `display(显示状态)`

```css
可以指定的值有				block 		inline-block 		none 		inline
分别将元素的表现形式指定为   块级   		行内块 			 消失			行内样式
```





### ` 标准盒模型与怪异盒模型`

>标准盒模型
>
>在这个模式下 我们设置的宽度和高度都是设置的content-box
>
>这会导致我们在设置内外边距和边框的时候需要考虑盒子的撑大问题 比较麻烦
>
>
>
>怪异盒模型 开启方式 box-sizing:border-box;
>
>``` 内容宽度+外边距(内容宽高包含了内边距和边框)```
>![enter image description here](https://img-blog.csdn.net/20160429135409319)

### `float(浮动)`

```css

 在html中 块级元素是默认占据一行的 

有些时候希望一行中可以存放多个块级元素

这个时候我们可以使用浮动 float 使元素脱离文档流

但是浮动布局会产生一种致命的缺陷 就是由于脱离了文档流 

会使父元素感受不到子元素 从而导致父元素的高度塌陷

解决这个的办法要不就是在父元素的末尾加一个专门用来清除浮动的div

要不就在父元素加上如下的样式

clearfix:after{

​	display:block;

​	content:" ";

​	height:0;

​	font-size:0px;

​	overfloat:hidden;

​	clear:both;

}
通过伪类来消除父元素的高度塌陷问题
```

### `background(背景)`

``` css
background(背景)是一条复合属性 渲染的顺序属性值分别为
color image repeat position/size
background-radius：数字+px；
设置圆角也有四个方向 顺序是左上 右上 右下 左下

```

### `position(定位)`

```css
定位这个属性很特别
他可以把元素定位到任何你想它去的地方
但是如果所有的元素都用这个属性的话是会非常消耗性能的
接下来说说定位的三个值 
position：relative；(相对定位)
相对定位是相对于元素本身定位的 可以使元素相对于自己本身的位置进行偏移
position：absolute;(绝对定位)
绝对定位是相对于父元素中第一个有定位属性的元素进行定位的
position:fixed;
这个属性定位是相对于整体的屏幕，即不会随着屏幕的移动而移动;
```

### `font(文字)`

```
color：颜色;可以设置文字的颜色
font-size：可以设置文字的字体大小;
font-weight:可以设置文字的粗细;一般属性值是整百的
font-family:可以设置文字的种类;可以设置多种字体 尽量用英文 如果前面的字体没有就会依次采用后续的字体
```

### `要做一个模态框的方法`

```
先用fix设置一个在窗口上固定的方框
给背景用rgba设置一个有透明度的颜色
或者用opcity设置一个透明度背景
```

### `如何制作一个文字水平和竖直都居中的盒子`

```
给盒子设置宽高
然后用text-align设置一个center
然后将line-height设置成与盒子高度一致 就行了
如果想盒子也在页面中居中的话 就需要用margin：0 auto；进行设置了
```

### `解析空格`

```
元素在我们平时的代码排版中 时常夹杂着回车或者缩进 在页面中会被浏览器自动的解析成为一个空格
这样会导致页面会多出现一些意料不到的空格
解决这个的方法就是在该盒子里面将字体的大小设置为0 这样空格就会消失
```

## `行内元素的对齐问题`

```
行内元素的经常会因为文字的位置或大小问题而导致对其的时候产生误差
所以说需要对文字的对其方式进行设置
需要用到vertical-align进行设置
可以使用的数值有 top middle base bottom 还可以用px值进行设置
```



