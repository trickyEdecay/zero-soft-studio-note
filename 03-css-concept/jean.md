# html相关语法知识
#### 1.<!DOCTYPE HTML>  最新版html的意思，html5标准网页声明
##### 2. <meta charset="utf-8">
     utf-8 默认设置，这样的网页打开才不会乱码
#### 3. <title>hello</title>    网页上面显示的内容**
#### 4. **<h1>title</h1>**    h1 一级标题  h2 二级标题----h6 六级
#### 5. <p title="hello">hello <span style="color:red">world</span></p>  
     style 属性 后面可以加属性名和值
#### 6.<a href="http://www.baidu.com" target="_blank" title="在新窗口中打开百度" >baidu</a>
    a 超链接 target="_blank"设定在新窗口打开 _self 设定在当前窗口打开
#### 7. <table border="3" cellspacing="0" cellpadding="10%">
- table是表格区 border+数字，数字代表表格的外框线层数，如果不加则没有外框线 
-   cellspacing 单元格与单元格之间的距离  
- cellpadding 单元格与内容的距离
   <table>
     <tr>  <!-- 行 -->
       <td>操作</td>   <!-- 列 -->
     </tr>
   </table>
#### 8. 表单标签form（包含menus、input、textarea、fieldset、legend、label）<form name=“user”  method=“get” >
     method 表单提交的方式，取值可以是get（提交少量数据）或post（提交大量数据）
##### <input placeholder="邮箱/昵称/账号名"  value="12315648@qq.com">

- input 空白输入框
- placeholder="这里输入的内容会在网页输入框里之间显示背景虚影"  
- value="12315648@qq.com" 这个会之间显示在输入框里，可以更改         
##### <input type="password" placeholder="输入你的密码"  >
- password 可以让你输入的内容全为点。 
- 加disabled则该输入框不能输入东西 
- 加readonly则输入框只能读
- 加maxlength则限制输入字符的个数
##### **<input id="sex_female" type="radio" name="sex"><label for="sex_female">女</label>**
     设置sex类，使两个选项选了一个其他另一个就不能选，去掉的话就都可以选  lable圆形选择框 
#####  复选框
     <input type="checkbox" name="food"><span>白菜</span>
     设置food类 span 矩形选择框
##### 重置按钮 
     <input type="reset" value="重新填写"> 
##### <input type="buttom" value="登录">
     作用主要是对表单进行提交
##### 下拉列表    
       <select  name="city“> <option value="汕头">汕头</option></select>
##### 文本区域
       <textarea  name="个人简介"  col=“宽度” row=“高度” ></textarea>

#### 9.块内元素 ：p  、h1-h6、 ul、ol、table、div、form
####    行内元素：img、a、input、button、label、textarea、select
******
# css 相关知识
### 1.在html中引入css的方法
>##### (1)嵌入式
><style type="text/css"></style>   同一个网页，<style>可以多次使用
>##### (2）外联式
><link rel="stylesheet" type="text/css"  href="http:\\img.jpg">
> <link>标记放在<head>标签里面
> rel：表示引入文件的类型
> ##### （3）行内式
> <h1  style="color:red;">
>

### 2.div:hover{background：red}--->鼠标放在div此区域时的颜色变红   div:active{} --->按住鼠标左键不松开的样式

### 3.对于文本类型的css的属性              
###### div{display：inline-block；background：blueviolet；color：red；padding：10px；text-align：center；line-height：40px；box-sizing：border-box；border-radius：5px；cursor：pointer；}
       1. display：规定网页元素如何显示问题，取值none（隐藏）block（以块元素显示）inline（以行内元素显示）inline-block（行内元素以块形式显示）
       2. padding：边框线到内容间的距离
       3. text-align：文本水平对齐方式，取值left、center、right
       4. box-sizing： border-box 指定宽度和高度来确定元素边框box
       5. line-height：行高
       6. border-radius：给元素设置圆角边框
       7. cursor：表示光标的类型 取值 text（形状I）help（形状？）wait（形状o） pointer（形状☝）
### 4. .选择器
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

#### 5.padding:10px 20px (上下10 px 左右 20px)    
    padding：5px 10px 15px 20px(上右下左)
#### 6.<span>ss</span> 起强调作用，是一个盒子型的行内元素。
#### 7. 每个标签都由属于自己的合适的元素，比如<font>标签就不能使用align这个属性，就算能用效果也显示不出来。
#### 8.父类中子类
>.b p:first-child{color:red;} <!--p(子元素)作为.b这个类(父元素)的第一项的加样式   *对应出现是last-child * -->
>.b h1:first-of-type{color:blue;} <!--h1(子元素)作为.b这个类(父元素)的出现第一次的加样式-->
>.b h1:nth-of-type(n){color:pink;} <!--h1(子元素)作为.b这个类(父元素)的出现的第n行的加样式-->
>.b h1:last-of-type{color:yellow;} <!--h1(子元素)作为.b这个类(父元素)的出现最后一次的加样式-->
>

#### 9.盒子模型（块级元素）
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
#### 10. 块级元素的class可以多个，而id只能有一个
  <div class="aa  bb"></div>
#### 11. 属性
         float：left/right (脱离文档流)
         position：static 静态  relative 相对位置，可以实现偏移（+left：10px；）  fixed 固定不随滚动框影响
         >absolute  绝对定位（脱离文档流）
         ```
         <div>（加position：relative）
              <div>加position：absolute，位置是相对于父元素div定位</div>
           <div>
          ```
          opacity：1（完全不透明）0（完全透明）
          若子元素margin>父元素margin，解决父子塌陷-》overflow：hidden；
          文字超出<div>用overflow：hidden（截掉超出部分）
          white-spacing：nowrap（文字不换行）
          letter-spacing：（字间距）

​          