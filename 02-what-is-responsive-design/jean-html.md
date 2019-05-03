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
