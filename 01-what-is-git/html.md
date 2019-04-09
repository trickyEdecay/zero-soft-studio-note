# html的学习
## 基本标签
####1. 标题
|标题        |符号       |
|:-------------:|:--------------:|
|一级标题        |<h1></h1>|
|二级标题        |<h2></h2>|
|三级标题        |<h3></h3>|
|四级标题        |<h4></h4>|
|五级标题        |<h5></h5>|
|六级标题        |<h6></h6>|
### 2.段落
```
<p></p>
<span></span>//修饰段落的某个字
```
### 3.超链接
```
<a href="网址"></a>
<a href="网址" target="_blank"></a>//开新网页
```
### 4.图片（自闭合标签）
```
<img width="100" height="100" str="图片地址">//一般width和height只设其一
<img alt="风景图" title="风景图2" src="图片地址">//图片地址不完整时，网络会崩
```
### 5.表格
```
<table>
     <tr>
         <td>操作</td>
         <td></td>
     </tr>
     <tr>
         <td></td>
     </tr>
</table>
//<tr></tr>为行，<td></td>为列
```
### 6.输入框（自闭合标签）
```
<input type="checkbox" checked="">//复选框,chackbox默认没有打钩,checked默认打钩
<input type="radio">//单选框
<input type="password">//密码框
```
```
<input placeholder="邮箱" value="123456">//placeholder只能用于输入框，value自动输入信息
<input type="password" placeholder="请输入密码" disabled>//disabled用于未输入上一步时，不让输入信息
```
```
<p>请选择你的性别</p>
<input type="radio" name="sex"><span>男</span>
<input type="radio" name="sex"><span>女</span>
//实现单选
```
```
<p>请选择你喜欢的运动</p>
<input id="sport_swimming" type="radio" name="sport"><lable for="sport_swimming">游泳</lable>
<input id="sport_running" type="radio" name="sport"><lable for="sport_running">跑步</lable>
//实现单选
```
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
### 值的不同写法
```
颜色的表示方式除了可以用英文单词red，还可以用十六进制#ff0000: p{color: #ff0000;}，还可缩写为p{color: #f00;}
```
### 基本语法
```
css声明总是以分号结束，声明组以大括号括起来
1.<h1 style="text-align: center; color: red;background color: blue;">
2.注释：/*这是个注释*/
### 引入外部的css
```
```
3.<link href="css/main.css" rel="stylesheet">
//link用的是href,而不是src，rel标签属性不能省略
```
### 块级元素和内联元素/行内元素
```每个标签都有自己默认的行为，自己会独占一行的标签元素叫做块级元素，，不会自己独占一行的标签元素叫内联元素/行内元素。
块级元素：p h1-h6 ul ol table div form
行内元素：img a input button label textarea select
两者区别：块级元素能够设计宽高，行内元素不行。
```
### 按钮
```
1.内边距
padding:10px,10px,5px,5px(上，右，下，左)
padding:10px,5px(上下，左右)
//0的话不要加单位px
2.外边距
margin:10px,10px,5px,5px(上，右，下，左)
margin:10px,5px(上下，左右)
```
```
<style>
   div{
       background: blue;
       color: #fff;
       border-radivs: spx;
       text-align: center;
       box-sizing: border-box;
       width: 90px;
       height: 40px;
       line-height: 40px;
       cursor:pointer;//光标移动到按钮时，会出现手指形状
   }
```







