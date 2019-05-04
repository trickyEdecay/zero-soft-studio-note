# JavaScript
### 1.基础数据类型
```
(1)string 字符串(" ")
(2)number 数字类型
- 数字类型特殊取值类型：infinity(为数字，正无穷),-infinity(为数字，负无穷),NAN(not a number)
(3)null 空值
(4)undefined 未定义  一个变量未定义时，默认值为undefined
(5)boolean (true/false)
```
### 2.高级数据类型
```
object(万物皆可onject)
```
```
function sayhello(){
    console.log("hello");
}
sayhello();//调用
另一种定义方法：
var sayhello;
sayhello=function(){
    console.log("hello");
}
sayhello();
```
```
var sayhello=function(){
    console.log("hello");
}
var b=sayhello;
b();
console.log(b===sayhello);
//true
```
```
function saywhat(){
    return function(){
        return "???";
    };
}

var a=saywhat();
var b=a;
console.log(b);
//???  （这三句可简写为console.log(saywhat()());）
函数可以返回任何一种类型，函数是object的一种子集
```
- 处理函数参数默认值：若用户不传参数，则默认值为undefined
### 3.基础数据类型间的转换
```
(1)number→string
a=1;//1
a=a+"";//"1"
或a=string(a);//"1"
```
```
(2)string→number
a="10";
a=number(a);//10
或parseInt(a);//10
```
```
parseFloat("1.1");//1.1,返回的是数字类型
parseInt("123abc");//123
number("123abc");//NAN
```
```
(3)string/number→boolean
①a=1;
boolean(1);//true
boolean(a);//true
boolean(0);//false
错误示范：boolean("true");//true
boolean("false");//true
②优化空间：1.var x="true";
            if(x==="true"){
                x=true;
            }else{
                x=false;
            }//true
          2.x="true";
            x=x==="true"?true:false  //true
          3.x=x==="true";  //最简单的string/number→boolean的方法
```
### 4.其他
```
(1)判断变量的所存类型： typeof a;
   ①历史bug: typeof null; //"object"
   ②a=1;
   typeof typeof a; //"string"
```
```
(2)判断是否为空：a===null;
```
```
(3)按值传递pass by ralue
a=1;
b=a;
console.log(a==b);  //true
a=2;
console.log(b);  //1
b不会被a=2影响
例如：tricky="知识";
     you="tricky";
     you=" ";
     console.log(tricky);  //知识
```
```
(4)判断一个变量是否为函数
var sayhello=function(){
    console.log("hello");
}
var b=sayhello;
console.log(typeof b);
```
```
(5)隐式转换：几个变量相加时，会隐式转换，只要有一个是字符串，则结果会为字符串
"10"+true;  //"10true"
10+true;  //11 (true为1)
10+false;  //10 (false为0)
10+null;  //10
10+undefined; //NAN
10+NAN;  //NAN
true+null;  //1 (转换为数字)
```
```
(6)输出年龄
var human={
    name:"mike",
    sex:"male",
    age:10,
    getOlder:function(){
        this.age++;
    }
};
human.getOlder();
console.log(human.age);
for(var index in human){
    console.log(key+":"+human[key]);
}
键值对：key value pairs
```
```
(7)
改变元素内容:
var myBtnEle=document.getElemById("my-btn");
myBtnEle.innerHTML="kiki";
改变css样式：
myBtnEle.style.backgroundColor="blue";
```
### 5.真值表
```
==和===的区别：前者不会比较数据类型，后者会比较
a=1;
b="1";
console.log(a--b); //true
console.log(a===b); //false
```
|a|b|==|===|
|:-----:|:-----:|:------:|:------:|
|undefined|undefined|true |true |
|undefined|false    |false|false|
|0        |null     |false|false|
|0        |0        |true |true |
|0        |false    |true |false|
|"0"      |0l       |true |false|
|" "      |null     |false|false|
|" "      |0        |true |false|
|" "      |false    |true |false|
|null     |undefined|true |false|
|null     |false    |false|false|
|null     |null     |true |true |
|NAN      |NAN      |false|false|
|1        |true     |true |false|
|true     |true     |true |true |
### 6.数组
- object的第二种：数组
- 定义空数组：var a=[];
- [ ]+12="12"
- [1,2]+12="1,212"
- typeof [1,2]
  ->"object"
- Array.isArray([1,2]);  //判断是否为数组
  ->true
- a.push()  //把最后一个进入
- a.pop()  //把最后一个弹出
```
var a=[1,2,"3",[1,3],function(){console.log("hello")}];
a[4]();//调用函数
console.log(a[4]);//打印出来函数体
console.log(a[3][1]);//取出a3的第一项
- 把a，b连接起来
var a=[1,2,3];
var b=[4,5,6];
a.concat(b);
var c=a.concat(b);
```
```
(1)var a=[1,2,3];  //a存的是内存地址
b=a;
console.log(b);  //[1,2,3]
b[1]=5;
console.log(b);  //[1,5,3]
console.log(a);  //[1,5,3]
a=[7,8,9];
console.log(a);  //[7,8,9]
console.log(b);  //[1,5,3]
(2)[ ]===[ ];
  ->false 因为地址不一样
```
```比较两个数组
function compareArr(arr1,arr2){
    if(arr1.length!==arr2.length){
        return false;
    }
    var result;
    for(var i=0;i<arr1.length;i++){
        if(arr1[i]!==arr2[i]){
            return false;
        }
    }
    return true;
}
```
```
输出数组的每一项数据类型
var a=[null,1,"2",[1,2],true,function(){}];
function outputTypes(arr){
    for(var i=0;i<arr.length;i++){
        if(Array.isArray(arr[i])){
            console.log("array");
        }else if(arr[i]===null){
            console.log("null");
        }else{
            console.log(typeof arr[i]);
        }
    }
}
outputTypes(a);
```
|a|b|==|===|
|:-----:|:-----:|:------:|:------:|
|[]     |undefined|false |false   |
|[]     |false    |true  |false   |
|[]     |null     |false |false   |
|[]     |0        |true  |false   |
|[]     |NaN      |false | false  |
|[]     |""       |true  |false   |
|[]     |[]       |false | false  |
|[1,2]  |undefined|false | false  |
|[1,2]  |false    |false |  false |
|[1,2]  |null     |false |false   |
|[1,2]  |0        |false | false  |
|[1,2]  |NaN      |false | false  |
|[1,2]  |""       |false | false  |
|[1,2]  |[1,2]    |false |false   |
# dom
### 1.获取元素的方法
- 获取一个元素
document.getElemById(" ");
- 获取多个元素(用class)
document.getElemClassName("类名");
- 特例
(1)获得body的元素
var bodyEle=document.body;或getElemByTagName("body");
(2)获得head的元素
var headEle=document.head;
- 获取父元素
console.log(pEle.parentNode);  //parentNode和parentElement是属性
- 获取子元素
var pEle=document.getElementById("类名");
var divEle=pEle.parentElement;
console.log(divEle,children[1]);
- 获取同胞兄弟
(1)console.log(pEle.previousElementSibling);  //输出上一个
(2)console.log(pEle.nextElementSibling);  //输出下一个
### 2.删除元素
- 删除div的p(要先获得要删除的元素和其父标签)
<div>
   <p id="abc">this is first</p>
   <p id="abc">this is second</p>
</div>

var pEle=document.getElementById("abc");
var divEle=pEle.parentElement;
divEle.removeChild(pEle);   //remove是方法
### 3.统计一个页面有多少个标签
function tagsCount(ele){
    var count=0;
    count=ele.children.length;
    for(var i=0;i<count;i++){
        var childEle=ele.children[i];
        console.log(childEle);
    }
    return count;
}
var bodyEle=document.body;
console.log(tagsCount(bodyEle));
### 4.判断当前结点的类型
var pEle=document.getElementById("abc");
console.log(pEle.childNodes[0].nodeType);
console.log(pEle.childNodes[1].nodeType);
if(pEle.childNodes[0].nodeType===3){
    
}
### 5.找到并去掉页面的注释结点
function cleanComments(ele){
    var childs=ele.childNodes;
    for(var i=0;i<childs.length;i++){
        if(childs[i].nodeType===Node.COMMENT_NODE){
            ele.removeChild(childs[i]);
            i--;
            continue;
        }
        if(childs[i].childNodes.length>0){
            cleanComments(childs[i]);
        }
    }
}
cleanComments(document.body);
### 6.创建元素
var divEle=document.getElementById("abc").parentElement;
var newPEle=document.createElement("p");
var helloText=document.createTextNode("hello");  //创建文本结点
newPEle.appendChild(helloText);      //创建文本结点
divEle.insertBefore(newPEle,divEle.children[1]);  //将创建的元素放在两个p之间，没有insertAfter
//createElement和appendChild是方法
### 7.修改标签
console.log(pEle.classlist)
console.log(pEle.className)
console.log(pEle.id)
console.log(pEle.classlist.add('d'));
console.log(pEle.classlist.remove('b'));
console.log(pEle.classlist.toggle('b'));   //有则删，无则加
### 8.将字符串变为小写
- 获得元素的标签名，返回的全是大写的
- tolowerCase 把整个字符串改为小写，是方法
"ABC".tolowerCase
->abc
### 9.获取title
var pEle=document.getElementById("abc");
console.log(pEle.title);
### 10.获取元素属性
- var imgEle=document.getElementById("pic");
console.log(imgEle.getAttribute("alt"));
imgEle.setAttribute("alt","修改内容");  //修改属性
- 获取imput的输入值
document.getElementById("suibian").value
设置imput的输入值
document.getElementById("suibian").value="设置的内容";
- 获取imput的勾选框
document.getElementById("suibian").checked
- 设置imput的能否输入
document.getElementById("suibian").disabled;  //默认值为true,不可用的
document.getElementById("suibian").disabled=false;  //改为可用的
- 去掉字符串的空格
if(newName.trim()===" "){
    return;
}
//return不用跟返回值
//消除左右两边的空格，不消除字符之间的空格
例："    ".trim();
  ->""
  "aaaa     ".trim();
  ->"aaaa"
  "    aaaa".trim();
  ->"aaaa"
  "     aa     ".trim();
  ->aa
  "     aa  aa    ".trim();
  ->"aa  aa"
### 11.控制链接的跳转
- location.href="http://www.baidu.com";
### 12.重新加载页面
- location.raload();  //raload是方法
### 13.隐藏的方式
(1)不脱离文档流
- visibility: hidden;  //存在位置，但不能与鼠标发生交互
- opacity: 0;   //设置透明度为0，存在位置，能与鼠标发生交互
(2)脱离文档流
- display: none;   //消失
### 14.事件控制
- 添加监听器
先获得这个元素: var attacjBtnEle=documentElementById("attack-btn");
attackBtnEle.addEventListener("click",attack);  //attack没有立即被执行
- 移除监听器
attackBtnEle.removeEventListener("click",attack); 
### 15.定时器与一些执行顺序的问题
- 定时器
setInterval(function(){
    console.log("hello");
},1000);
//1000=1s,1000*60*60=1小时
另一种表示方式:
setInterval(hello,1000);
function hello(){
    console.log("hello");
}
- 执行顺序的问题
console.log("hi");
setInterval(function(){
    console.log("hello");
},1000);
console.log("hey");
->hi
 hey
 hello
//hey不会等到hello调用完才执行，而是直接执行
### 16.cookie、localstorage
```
保存信息在浏览器端，都独立于网址，cookie独立于浏览器，只在设置的cookie过期时间之前一直有效，即使窗口或浏览器关闭，换一个浏览器则不会显示保存信息，cookie数据不能超过4k，而localstorage则可以达到5M，localStorage的数据有效期是始终有效，窗口或浏览器关闭也一直保存，因此用作持久数据。
```