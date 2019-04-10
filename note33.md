#1.选择器
##细节一
h2,p(称为选择器列表)  
{
}  
h2 p(后代选择器)  
{
}    

#上课开始
##css
border-radius:5px){

}(圆角5像素)
###伪类选择器 
 
.button:active{
background:blue
}(鼠标按下下去后有蓝色)

.button:hover{
background:red
}(鼠标悬停有红色)

a:link{
color:red
}（链接变成红色）

a:visited{
color:yellow
}（点击链接后变成黄色）  

a:focus{
outline:none
}
.a span:first-child{

}(出现在第一个还要第一项才被匹配)

.a h1:first-of-type{

}(出现第一次h1第一项被匹配)
> outline作用是去掉焦点边框  

li:nth-of-type（填写数字）{
background:red;
}(无序列表中的填写数字的背景红色)

>  ** 伪类选择器有顺序**  
###获得焦点
tabindex="正整数"
> 正整数部分必须排序


##3.盒子模型
> 行内元素不可包裹块级元素
###1.conternt area
内容
###2.padding
内间距
###border
边际
###margin
外边距（两个元素之间的距离）
##border-radius
圆角
> border-radius=宽高像素就会变成一个圆形

###外边距的合并
相邻兄弟块级元素的合并（取最大值）
###行内元素
不能设置padding和margin
###margin
子元素和父元素margin合并
###可替换元素和不可替换元素

###行内块
display:inline-block（无视行内元素和块级元素）

display:block(将行内元素设置为块级元素)

vertical-align:baseline

line-height:
 ###块级元素居中
mergin:0 auto;  

#css 后代选择器
|代码|功能|
|---|---|
|.button:active{color:blue}|鼠标按下后拥有蓝颜色|
|.button:hover{background:red}|鼠标悬停的时候背景为红色|
|a:link{background:red}|链接背景变成红色|
|a:visited{color:blue}|浏览过后字体颜色变为蓝色|
|a:focus{outline:noe}|屏幕焦点没有东西|
|h1 span:first-child{}|不仅需要第一个子元素还要子元素里面排第一个才被匹配|
|h1 span:first-of-type{}|子元素中排列第一个span元素就会被匹配|
|li:nth-of-type(填写数字){}|无序列表中填写的数字的属性|





