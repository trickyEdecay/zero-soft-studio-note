# JavaScript：
引入要用src

```js
var a;  //varity（多样性）
alert(); //弹出
console.log();   //控制台输出
```



**基础数据类型：**
string
number：infinity（正无穷） - infinity（负无穷）  NaN（not a number）
boolean
null
undefined
symbol



isNAN()    是  不是数字？

== 不会比较类型
=== 会比较类型

| a         | b         | ==   | ===  |
| --------- | --------- | ---- | ---- |
| undefined | undefined | T    | T    |
| undefined | false     | F    | F    |
| 0         | null      | F    | F    |
| 0         | 0         | T    | T    |
| 0         | false     | T    | F    |
| 0         | NaN       | F    | F    |
| "0"       | 0         | T    | F    |
| ""        | null      | T    | F    |
| ""        | 0         | T    | F    |
| ""        | false     | T    | F    |
| null      | undefined | T    | F    |
| null      | false     | F    | F    |
| null      | null      | T    | T    |
| NAN       | NAN       | F    | F    |
| 1         | true      | T    | F    |
| true      | true      | T    | T    |
| []        | []        | F    | F    |
| [1,2]     | [1,2]     | F    | F    |



typeof   不是一个函数，是一个一元运算符，返回一个变量的类型。



string()： 将数据类型转化为字符串。

number()：将字符串转化为数字       字符串中的字符必须全部为数字才能转化。

​							    若不是全部为数字，会转化为NaN

parseInt()：将字符串转化为数字      不一定要全部为数字，第一个需为数字

boolean()：转化为布尔值



##### 函数的定义与调用：
```js
1.
	function sayHello(){
		console.log("hello");
	}
	sayHello();
2.
	var sayHello;
	sayHello = function (){
		console.log("hello");
	}
	sayHello();
```
##### 数组的一些操作：
```
Array.isArray();   判断是否为数组

var a = [1 , 2 , 3];

a.push(5);    数组尾部添加一个数据。

a.pop();     弹出最后一个数据。

var b = [4 , 5 , 6]

var c = a.concat(b);

```
##### 对象：
```js
var human = {};   //新建对象
human.name = "ss";
human.age = "18";
human.hello world = "hello";

//key value pairs
//键名有空格，则键名需加双引号
var human = {
    name:"ss",
    age:18,
    "hello world":"hello",
    getAge:function(){
        console.log("this.age");
    }
};

console.log(human["hello world"]);
console.log(human.name);
```

>javascript中如果获得的是一个html元素，变量命名后缀需为Ele
>document不是javascript语言本身。



**Math下的方法：**
floor ceil round



# DOM操作：


```js
document.getElementById("")		//根据ID获得元素
document.getElementsByTagName("")      //根据标签获得元素
document.getElementsByClassName("")   //根据class获得元素
document.querySelector(" css中的选择器 ")     //根据选择器获得元素

document.body	//可以直接获得body元素
document.head	//可以直接获得head元素

parentNode   // 取得一个元素的父元素
parentElement

children     //取得一个元素的子元素  (多个都会被取到)
childNodes     //不被标签修饰的可以称为文本结点
nodeType    //取得结点类型    
			//3：文本结点   1： 元素结点  8:comment结点（注释的内容）
			//Node.TEXT_NODE     3
			//Node.ELEMENT_NODE  1
			//Node.COMMENT_NODE  8

nextElementSibling    //取得一个元素的下一元素（同胞元素）
previousElementSibling    //取得一个元素的上一元素（同胞元素）

createElement("标签名");   //创造一个新的标签
父元素.appendchild(创造的元素);
createTextNode("文本内容");
insertBefore(新的标签，要插入在其之前的标签)
```



**获得元素的id或者class：**
```
.id
.className
.classList
```

**获取input的一些信息：**
```
.value  //获取input输入的内容
.checked //获取勾选框的状态
.disabled  //改变文本框是否可修改
```

imgEle.getAttribute('alt');    //获取元素的属性
setAttribute( 'alt' , "要修改");

>删除一个元素：先取得这个元素，再取得其父元素，父元素再调用removeChild方法删除指定子元素。
removeChild()     

trim()    // 删除左右两边的空格 (获取用户输入可用到)




##### 链接的跳转与页面的重加载：
location.href("http://www.baidu.com")   //跳转
location.reload()   //刷新



##### 事件的控制：
addEventListener("click",attack);      //添加事件监听器

removeEventListener("click",attack);     //移除事件监听器



DOM Interface   文档对象模型接口

Document Object Model - 文档对象模型



##### 定时器：
```js
var timer;
timer = setInterval(function(){

},1000);
clearInterval(timer);


//延迟执行
setTimeout(function(){

},1000); 
```


##### 本地缓存：
cookie
localStorage          // setItem( key , value )     getItem(key)



# css的一些补充：

##### 字体样式：

monospace 等宽字体
serif  衬线字体
sans-serif  无衬线字体

##### 控制为不可见：
```css
.class{
    visibility:visible;
    opacity:0.0;
    diaplay:none;
}
```
##### 动画效果：
```css
transition:width .2s ease-in-out;       //ease-in-out：规定以慢速开始和结束的过渡效果
```