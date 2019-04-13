#1.标签
##html标题
<h1>我的第一个标题</h1>    
   
- 默认左对齐       
+ align="center"居中对齐    
* align="right"向右对齐    
  
##html段落
<p>我的第一个段落</p>
##html连接

'''
<a href="http://www.baidu.com">这是百度</a>
'''
##html图片
 <img src="https://i.loli.net/2019/04/07/5ca9a71a34bf6.jpg">

>一般标签需要开始和结束标签如<h1></h1>
##html换行
br
##html表格

table
> table border="1"表示间隔1  
th表示行  
td表示列  
##关于input
-密码  
<input type="password(密码字段)"name="password"（密码名称)>
***     
+单选按钮  
<input type="radio" （单选按钮）name="sex"（按钮的名称)value="female"（按钮的值...） 
***
*复选按钮
 <input type="checkbox"(复选按钮)name="car"(复选按钮名称)value="bike"(复选按钮的值)>
***
文本  
User(显示内容)<input type="text"(文本域)name="User"(文本名称)>
提交按钮  
<input type="submit"(提交按钮)value="submit"（提交按钮的值）>  

#2.html结构
##一.!DOCTYPE html
表示为html5
##二.html 
表示为html页面得元素
##三.head
表示为文档数据，
###head里面属性
 定义网页编码格式为 utf-8  
![格式](https://i.loli.net/2019/04/07/5ca9a533db411.png)  
tittle表示为文档标题
![title](https://i.loli.net/2019/04/07/5ca9a474af275.png)
##四.body
写html正式内容
#3.属性
> 在标签内直接设置属性
##class
表示**类型**例如青年，青少年，成年人
> 使用方法:.car(名称)
##id
ID  
起码**身份证**效果
> 使用方法:#car(名称)
##style
行内样式多写于head
##title
元素额外信息
##target
target="_blank"  在浏览器新窗口打开文档  
target="_self" 在本窗口打开文档  
##alt
**加载图片出错显示内容**
##title
**鼠标悬停会显示图片内容**
##name
**元素的名称**
##type
定义元素类型比如radio,button
##span
给元素添加额外属性比如color

#4.CSS
用<link rel="stylesheet"href="suibian.css"(文件名)type="text/css" >导入
##基本选择器 
 
- 标签选择器
+ p{color:green}
- id选择器
+ #sex{font-size:30px；}
- class选择器
+ .sex{background:#000000}
- 后代选择器
+ p span{color:blue}
+ ***
 


