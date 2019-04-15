# css 样式
### 1.选择器
##### 标签选择器 
     如：h1{color:red;} h1，p{color:red;}中 h1，p表示选择器列表  h1 p{color:red} 中h1 p表示后代选择器，意思是h1中包含的p标签。
##### class选择器 
     如：.box{color:red;}
#####  id选择器 
     如：#box{color:red}
##### 伪类选择器(修饰已经完整的网页元素的效果)
> 1. a:link{color:red;}
> 2. a:visited{color:blue;}
> 3. a:hover{color:yellow;}
> 4. a:active{color:pink;}
> 伪类选择器这四个标签必须得按照1到4的顺序写，如果不按照此顺序，标签里面的效果可能会被覆盖掉。
> 

> .box:foucs{color:red} <!--对元素获得焦点设置的命令，但是不是所有的元素都能设置焦点(input 可以获焦)-->
> <input class="a1" tabindex="1">
> <div class="box"  tabindex="2" >qq</div>
>  <p class="aa"  tabindex="3">订单</p>
>   <input class="a"   tabindex="4" >
> 对.a1:foucs{border:1px solid red;}和a:foucs{border:1px solid red;}进行获焦，中间隔了两行，用如上所写tabindex（顺序选择）进行排序选择，然后在网页点击文本框后键盘上按tab健能够实现.a1到.a 的聚焦。
> 

#### 2.padding:10px 20px (上下10 px 左右 20px)    
    padding：5px 10px 15px 20px(上右下左)
#### 3.<span>ss</span> 起强调作用，是一个盒子型的行内元素。
#### 4. 每个标签都由属于自己的合适的元素，比如<font>标签就不能使用align这个属性，就算能用效果也显示不出来。
#### 5.父类中子类
>.b p:first-child{color:red;} <!--p(子元素)作为.b这个类(父元素)的第一项的加样式   *对应出现是last-child * -->
>.b h1:first-of-type{color:blue;} <!--h1(子元素)作为.b这个类(父元素)的出现第一次的加样式-->
>.b h1:nth-of-type(n){color:pink;} <!--h1(子元素)作为.b这个类(父元素)的出现的第n行的加样式-->
>.b h1:last-of-type{color:yellow;} <!--h1(子元素)作为.b这个类(父元素)的出现最后一次的加样式-->
>

#### 6.盒子模型（块级元素）
- 此模型中适应background:yellow ;填充颜色，在盒子模型中填充的部分（content+border+padding）
- border-radius:100px等价于 width:100px;height:100px;  
- 行内元素也适用盒子模型，但不设padding-top/bottom，margin，而且不可设width和height，就算设置了，效果也显示不出来。
- 外边距的合并和折叠
   >   出现在兄弟元素（同级）块级元素之间
   >>  如：块元素---上元素的margin-buttom与下元素的margin-top，如果两个值一样，会出现重合，如果不一样，则取值比较大的。
- 父元素和子元素的合并
  >原理：块元素包含行内元素  <!--行内元素不能包含于块元素-->
  >块元素（上下之分） 行内元素（左右之分）

- 可替换元素 
     以行内元素为例（宽高有字长决定；）img 能写出标签但是想象不出来样子就是可替换的；
- 不可替换元素（行内元素：宽高由内容决定）
- 行内元素--->块元素
       display：block； 变成块
       display：inline-block；变成行内块
- 块元素-->行内元素
       display：inline-block； 变成行内块；
- ![基线](https://i.loli.net/2019/04/12/5cb07f6686c21.png)
  > 1. 如图上所言，黑色圆的底部与红色区域底不重合，把红色区域比作四线本，四
  > 线本的第三条线与黑色圆的底部叫做基线（baseline），红色的底部也就是基线下面那条线叫做bottom。
  > 2. 一般情况下可替换元素的底部都有基线，并且基线不是固定位置，是会变动的。
  > 3. 要实现baseline和bottom重合，需要在黑色圆的css样式下加
  >    vertical-align:bottom（默认baseline与bottom对齐）
  >    

- 实现块级元素居中
       1. margin：0  auto
       2. margin-left的值等于margin-right

