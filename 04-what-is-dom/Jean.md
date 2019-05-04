# html dom操作（文档对象模型）
### 节点：元素[标签]节点、文本节点和属性节点
```
1. 标签节点 就是html里的标签，如<body>、<p>之类的标签。标签的名字就是元素的名字
2. 文本节点 就是文本，如<p>标签包含this is content文本，那么这个文本就是文本节点
3. 属性节点 被放在起始标签里，如<p title="title">xxxx</p>，那么title="title"就是属性节点
```
#### 1. getElementById(id);(通过 id 查找 HTML 元素)
查找 id="main" 元素(节点上设置id属性，id应该设置为独一无二的，但是你非得在html节点上加上两个相同的id，chrome上只会返回第一个。)
`var x=document.getElementById("main");`
#### 2.getElementsByTagName(tag);(返回包含带有指定标签名称的所有元素的节点列表（集合/节点数组）)
- document.getElementsByTagName("*"):返回文档所有元素节点
- 查找 id="main" 元素中的所有 <p> 元素：
`var x=document.getElementById("main").getElementsByTagName("p");` 

#### 3.getElementsByClassName(class)(通过class属性来访问元素),返回的也是数组。
- 支持多个class 类
`document.getElementsByClassName("name1 name2")`
#### 4.getAttribute()、setAttribute();（用来获取和设置节点上的属性）
- 获取`<img>`其他元素属性
    var imgEle=document.getElemById("pic");
    imgEle.getArribute("alt");
- 设置`<img>`其他元素属性
    var imgEle=document.getElemById("pic");
    imgEle.setArribute("alt"，“风景”);
#### 5.childNodes获取节点下的所有类型的子元素,返回一个数组
- 节点包括元素节点、文本节点，属性节点，甚至连空格和换行都会被解释为节点
- childNodes返回所有类型的节点，我们可以通过nodeType获取节点的类型，但是该属性只返回整型
> nodeType 节点的类型
 >元素节点的nodeType属性值是1.
 >属性节点的nodeType属性值是2.
 >文本节点的nodeType属性值是3.
 >注释节点的nodeType属性值是8.

 - <u>注：区别于getElementsByTagName("")</u> 
> getElementsByTagName("")返回的不仅仅是直接子节点，如果子节点包含了节点，也会计算在内的。
>

- nodeValue 属性返回文本节点的值 
> document.getElementById("main").childNodes[0].nodeValue;//document.getElementById("xxx").firstNode.nodeValue;
> 

- nodeValue除了可以获取文本节点的值，还可以修改文本节点的值
> p.firstChild.nodeValue = "通过nodeValue设置新的值"
> 

####  6.节点访问关系（以p标签访问为例）
- 访问p的父节点 p.parentNode;
- 访问p的子节点 p .childNodes;(包含文本节点（空格和换行))
- 访问p节点中的所有**元素子节点** p.children
- 访问p的兄弟节点  p.nextElementSibling;
- 访问p前一个兄弟元素节点 previousElementSibling
#### 7.添加子节点
 ###### 从后面添加：节点.appendChild(传入的节点)  作用：用于添加新元素到尾部 

- 以下代码是用于创建 `<p>` 元素:
 var para = document.createElement("p");
- 为 `<p> `元素添加文本节点：
var node = document.createTextNode("这是一个新的段落。");
-  将文本节点添加到 `<p> `元素中：
para.appendChild(node);
-  最后，在一个已存在的元素中添加 p 元素。
    查找已存在的元素：
    var element = document.getElementById("div1");
    添加到已存在的元素中:
    element.appendChild(para);
 ###### 从前面添加：节点.insertBefore(要插入的节点 , 在谁之前); 将节点插入到子节点中指定节点的前面。 
 `<p id="p1">这是一个段落。</p>`
  var child = document.getElementById("p1");
  element.insertBefore(para, child);
#### 8. 删除节点 
父节点.removeChild(子节点) 
#### 9.替换节点 replaceChild(); 
替换节点：父节点.replaceChild(新节点，要替换掉的子节点);
#### 10. classlist
- html :`<p class="a b c"></p>`
js: var pEle= document.getElementById("p");
 console.log(pEle.classList);
 结果：![图](https://i.loli.net/2019/05/02/5ccae0333b0db.png)
是一个类似数组的对象
- pEle.classList.add("dying");//添加class样式类"dying"
- 区别于className，console.log（pEle.classname）结果是字符串
#### 11.增加用户监听器 addEventListener() 
- 在用户点击按钮时触发监听事件
 document.getElementById("myBtn").addEventListener("click", displayDate);
- ` var element= document.getElementById("myBtn")；`
 ` element.addEventListener(event, function, useCapture);`
>第一个参数是事件的类型 (如 "click" 或 "mousedown"). 
第二个参数是事件触发后调用的函数。 
第三个参数是个布尔值用于描述事件是冒泡还是捕获。该参数是可选的。

- 向同一个元素中添加多个监听事件
 element.addEventListener("click", myFunction);
 element.addEventListener("click", mySecondFunction);
#### 12.移除监听器 removeEventListener() 
  element.removeEventListener("mousemove", myFunction);
#### 13.cookie与localstorage
![区别](https://i.loli.net/2019/05/04/5ccd90fae2d9e.png)
```
localStorage.setItem("key","value");//以“key”为名称存储一个值“value”

localStorage.getItem("key");//获取名称为“key”的值
```
#### 14.获取 input 的输入值、设置 input 的输入值
 - 获取 input 的输入值  input.value
# JavaScript知识 
##### 1.JavaScript 计时事件
 -  setInterval() - 间隔指定的毫秒数不停地执行指定的代码。
 > setInterval(函数名,毫秒数);
 > var myVar=setInterval(function(){myTimer()},1000);
 >

- clearInterval() 方法用于停止 setInterval() 方法执行的函数代码
>clearInterval(myVar);
>

- setTimeout() - 在指定的毫秒数后执行指定代码。
   myVar=setTimeout(function(){alert("Hello")},milliseconds); 
- clearTimeout() 方法用于停止执行setTimeout()方法的函数代码。
     clearTimeout(myVar);

##### 2.js五种基本数据类型
```
null、undefined、number、string、boolen
```
##### 3.变量
```
 a=Infinity(数字)->正无穷
 a=-Infinity(数字)->负无穷
 a=NaN->不是数字
```
typeof a; 看a的数据类型
```
typeof  null；->输出："object"；
typeof  a；->输出："number"；（a=2;)
typeof  typeof a；->输出："string"；
```
##### 4.类型转换
- parseInt("123abc")->123
- paatseFloat("1.2")->1.2
- Number("123abc")->NaN
##### 5.隐式转换
```
 123+"123"+123->"123123123"
 "10"+true->"10true"
 10+true->11 / 10+false->10 / 10+null->10
 10+undefine->NaN
 true+null->1
 [1,2]+12->"1,212"
```
Math.floor(1.1)->取整
Math.ceil(1.2)->2
Math.round(1.8)->四舍五入

