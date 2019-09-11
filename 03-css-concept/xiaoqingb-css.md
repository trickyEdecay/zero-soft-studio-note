# CSS

上节课回顾：

- alt 裂了显示

- 标签属性

- h2，p{

- 这是选择器列表

- }

- h2 p{迭代选择器｝

- style 不要加type，避免写错

## 一.伪类

### 1.link-visited-hover-active （伪类选择器）l v h a

- link修改链接颜色属性
- visited访问过可以显示某种颜色
- hover悬浮特效
- active 活动特效

### 2.outline：none 

去掉焦点棱角边框

### 3.focus（伪）

点击输入时输入框会变色，加特效

有些不能选择或输入的

也可以在属性里加 tabindex=“1/2/3” 这样也能转换成焦点，注意是有顺序的

### 4. first-child  first-of-type

```css
a span:first-child{}
```

  必须是父元素的第一项span  span必须放在第一行  第二行就会失效

```css
a span:first-of-type{} 
```

   span不用再第一行

### 5.last-child  last-od-type (就是跟上面反过来)

### 6.:nth-of-type

```css
li:nth-of-type(){

括号里填n就是所有整数项，2n就是偶数项，20-1就是奇数项，也可以直接写成是第1、2、3项

}
```



### 7.标签不能用纯数字开头

### 8.伪类选择器叠加  

a:nth-of-type:hover{}

推荐把hoverfanghoumian 

# 二.盒子模型

### 1.content-area

### 2.padding

### 3.border

### 4.margin

#####  外边距的折叠

* 相邻的相邻兄弟元素（块级）之间的margin会重叠，塌陷，合并
* 当父元素和子元素的margin的值不一样时，会取最高值
* 当父小于子时，加个solid black会自动把border拉到父的margin边缘

### 5.border-radius 

圆角  设置成等于盒子宽高一样就变变成圆圈

### 6.不要给行内元素设置 padding

### 7.可、不可替换元素

##### 可替换元素

看内容多少

##### 不可替换元素

img，input  这种写了标签，但是想象不出来是啥样的，图片大小是未知的

### 8.文档流

从上到下，从左到右 

### 9.行内元素不能包含块级元素

严重不规范的行为！！！

### 10.行内元素不能设置宽高

行内块就能设置宽高

### 11.inline-block

无视行内元素宽高设置
```html
<!DOCTYPE html>
<html>
<head>
	<title></title>
	<style>
		.kuai{
			display: inline-block;
			width: 50px;
			height: 50px;
			border-radius: 50px;
			background-color: red;
			text-align:center;
			line-height: 50px; 
		}
		.kuai:hover{
			background-color: yellow;
		}
	</style>
</head>
<body>
<div class="hang">
	<div class="kuai">123</div>
	<div class="kuai">123</div>
	<div class="kuai">123</div>
	<div class="kuai">123</div>
</div>

</body>
</html>
```





![1554888756201](C:\Users\xiaoqingbbbb\AppData\Roaming\Typora\typora-user-images\1554888756201.png)

上面圆形之间会有缝隙，可以把父元素的margin设置成0.子元素margin设置成自己想要的

另一个方法是将子元素margin设置成负的



### 11.baseline

基线

### 12.vertical-align 设置对齐

vertical-align：baseline；

在子元素里加vertical-align：bottom；

![1554889537610](C:\Users\xiaoqingbbbb\AppData\Roaming\Typora\typora-user-images\1554889537610.png)

![1554889665995](C:\Users\xiaoqingbbbb\AppData\Roaming\Typora\typora-user-images\1554889665995.png)

### 13.position

- static  已经是默认的
- absolute  绝对位置，脱离文档流
- relative 相对位置，相对父元素的位置，没有脱离文档流
- fixed  固定在窗口的位置，滚动滚动条也还是在哪个位置

### 14.bo-sizing:border-box



### 15.opacity(透明度)

联合fixed使用，就是加一层灰灰的，显示内容为同级内容

`position:fixed;
  opacity:0.5;`

### 16.Float

当块级元素设置了float时，变成了行内元素，但还是会推开文字流

float外边距不会塌陷

inline-block会塌陷

### 17.block

用absolute后就会自动转化为block

### 18.使用overflow:hidden，float，absolute，fixed时

产生一个BFC，在内部无论怎么调，都不会影响外部

overflow:hidden相反的时overflow:visible

hidden 要配合text-overflow:ellipsis , white space：nowarp 应用于单行

### 19.overflow:scroll

滚动条

正文14px-16px 

提示文字减2

### 20.font-family:"字体"

百度张鑫旭有字体中英文对照表

如果字体写两个，会默认第一个，找不到才会用第二个

一般最后加个 sans-serif  无衬线字体     cursive  minisoace（等宽字体 ，写代码，涉及银行）

font-weight 

一般取100-900  整百取的，不是所有字体都有粗细的

### 21.letter-spacing 

字间距

### 22.text-decoration: underline/none

加下划线效果，或者可以用border-bottom

### 23.white-space:nowrap

无视框的长度，直接显示一行

### 24.空格

`&nbsp`

### 25.转义符&

用到再查转义表  

### 26.overflow-x/y :auto

当溢出时，自动出现X或Y滚动条

### 27.calc

用于计算百分比减去固定长度

### 28.em

用于使用在line-higeht上，1em等于font-size的大小

### 29.一个200px×200px父元素包了一个宽高都为100%的子元素

- 父元素的可分配空间就是它的content-box大小+padding大小

- 子元素的100%指的是它的content-box大小跟父元素的content-box一致

- 父元素有padding，子元素的100%还是父元素的content-box

- 子元素的100%会受到父元素box-sizing设置padding的影响

- 子元素的100%会受到子元素box-sizing设置padding的影响

  

# 三.弹性布局

#### flex

父元素设置flex，变成了弹性布局容器，直属的子元素为Flex item

- flex-direction:cplumn主轴方向为纵向，row为横向 row-reverse横向反向 

- flex-wrap:wrap  （warp-reverse）自动换行，默认值是nowrap   设置第二条轴叫做交叉轴

#### justify-content:center  

控制主轴元素对齐方式  有flex-star/end,space-between(自动分配空间填补空格)

#### align-item:center

- 默认值是stretch· 子元素没有设置宽高时会被拉伸（）

- item 的交叉轴跟父元素对齐方式

- 还可以设置值为baseline

- 主要用于图片垂直居中



#### align-content:flex-start

- 多根主轴在交叉轴上的对齐方式



#### flex-basic

子元素在主轴上的尺寸

#### flex-shrink：0/1

默认设置成1,相当于占用一个子元素，设置成2时就是两个子元素



#### flex-grow:1/2/3

- 自适应占用几个格去去平均分配

- 默认值是0

#### 简写：flex：0 1 40px（grow thrink basic）

## 四.FFC-flex formatting context 弹性布局上下文

## 五.BFC 块级布局上下文

## 六.设置标签属性无效

- 检查class的双引号
- 检查名字是否一致
- 检查是否有保存
- 



作业  

右边在去加几个按钮

用弹性布局写导航栏

学习js

学习bootstrap



>  




```

```