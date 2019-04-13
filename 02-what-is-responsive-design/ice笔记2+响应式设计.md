# 笔记2


## 插入文本框标签input

> input是一个自闭合标签
> <input> 标签用于搜集用户信息。
>根据不同的 type 属性值，输入字段拥有很多种形式。输入字段可以是文本字段、复选框、掩码后的文本控件、单选按钮、按钮等等。   

```html
<input />
```
>但由于规范问题，可将==/==省去。  

|type属性|描述      |
| :------- | ---- |
| checkbox |定义复选框。      |
|  radio   | 	定义单选按钮。      |
|   password       |定义密码字段。该字段中的字符被掩码      |
|button   |定义可点击按钮 |



|placeholder属性| 描述     |
| :--- | :--- |
|placeholder|placeholder 属性提供可描述输入字段预期值的提示信息。该提示会在输入字段为空时显示,并会在字段获得焦点时消失|



| value 属性| 用法     |
| ---- | ---- |
|type="button", "reset", "submit"|定义按钮上的显示的文本      |
|type="text", "password", "hidden"| 定义输入字段的初始值     |
|type="checkbox", "radio", "image"|定义与输入相关联的值      |



|disabled属性| 描述     |
| :--- | :--- |
|disabled|被禁用的 input 元素既不可用，也不可点击。|



## label 标签

><label> 标签为 input 元素定义标签（label）。
>label 元素不会向用户呈现任何特殊的样式。不过，它为鼠标用户改善了可用性，因为如果用户点击 label 元素内的文本，则会切换到控件本身。
><label> 标签的 for 属性应该等于相关元素的 id 元素，以便将它们捆绑起来。

|label属性| 描述     |
| :--- | :--- |
|for| 规定 label 绑定到哪个表单元素。|





## css

1. 内联样式表(==不推荐使用==)

2. 内部样式表(写在***head的style标签中***)

3. 外联样式表（添加代码`<link rel="stylesheet type="text/css href="*.css">`将css样式引入到HTML文件中,==结构与表现分离，推荐使用==)

   

>css中有许多属性，详情可上网搜索



## 选择器

1. 标签选择器      (标签名{})
2. 类选择器   (`.class{}`)
3. id选择器     ( `#id{}`)
4. 后代元素选择器(祖先元素 后代元素)
5. 子元素选择器（父元素 >子元素）
6. hover选择器（:hover）用于选择鼠标指针浮动在上面的元素。
7. active选择器(:active)  用于活动链接



## 优先级

1. id选择器>class选择器>标签选择器

2. 内联>内部>外联


>***!important***   可以修改优先级，优先级最高，但在实际开发中==不推荐使用==



## 块元素和行内元素

> 块元素主要用来做页面布局，行内元素主要来选中文本设置样式

>常见的块级元素:p h1-h6 ul ol table div table

>常见的行内元素:img a input button label textarea select
>
>

区别:
1. 块级元素能设置宽高，行内元素不行。

2. 块级元素独占一行，行内元素不会

3. 块级元素对应display:block，行内元素对应display:inline。可以通过修改元素的display属性来切换行内元素和块级元素。

   

## 盒子模式
![盒子](https://ss0.baidu.com/6ONWsjip0QIZ8tyhnq/it/u=187675152,3794847365&fm=173&app=25&f=JPEG?w=640&h=389&s=EE6DB85612FE0588507F547C03007073)
![盒子](http://img.smyhvae.com/20170727_2128.png)



盒子实际宽度（高度）=内容（content）+边框（border）+间隙（padding）+间隔（margin）。对于任何一个元素设置width和height控制内容大小，也可以分别设置各自的边框（border）、间隙（padding）、间隔（margin）。灵活设置这些盒子的这些属性，可以实现各自排版效果。





## 响应式设计

>使用 @media 查询，你可以针对不同的媒体类型定义不同的样式。

>@media 可以针对不同的屏幕尺寸设置不同的样式，特别是如果你需要设置设计响应式的页面，@media 是非常有用的。

>当你重置浏览器大小的过程中，页面也会根据浏览器的宽度和高度重新渲染页面。
>
>

```css
@media screen and (max-width: 300px) {
    body {
        background-color:lightblue;
    }
}
```
>如果文档宽度小于 300 像素则修改背景颜色为蓝色。