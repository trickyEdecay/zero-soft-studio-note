# DOM操作

> 文档对象模型( DOM, Document Object Model )主要用于对HTML和XML文档的内容进行操作。
>
> DOM描绘了一个层次化的节点树，通过对节点进行操作，实现对文档内容的添加、删除、修改、查找等功能。
> 



## DOM的节点

> 节点：

1. 文档节点

2. 元素节点

3. 属性节点

4. 文本节点

   

> 节点属性：
 1. nodeName
 2. nodeType
 3. nodeValue




## 获取元素节点

#### 通过document对象调用

1. getElementById()       

   通过==id==属性获得==一个==元素节点对象

2. getElementsByTagName()

   通过==标签名==获得==一组==元素节点对象

3. getElemenstByName()

   通过==name==属性获得==一组==元素节点对象

4. getElemenstByClassName()

   通过==classname==属性获得==一组==元素节点对象

5. querySelector()

   通过==选择器==获得==第一个匹配==元素节点对象

6. querySelectorAll()

   通过==选择器==获得==所有匹配==元素节点对象

   

 <!---有括号是方法，没有括号的是属性，注意区分，下文同-->



## 获取元素节点的子节点

####  通过具体的元素节点调用

1. getElementsByTagName()

   返回当前节点的指定标签名的后代节点

2. childNodes

   表示当前节点的所有子节点，包括由于空格引起的文本节点

3. firstChild

   表示当前节点的第一个子节点

4. lastChild

   表示当前节点的最后一个子节点



<!--以上不完全全面，有需要请百度-->



## 获取父节点和兄弟节点

#### 通过具体的节点调用

1. parentNode

   表示当前节点的父节点

2. previousSibling

   表示当前节点的前一个兄弟节点

3. nextSibling

   表示当前节点的后一个兄弟节点

   

<!--特例：document.body/head-->



## DOM的添加节点
|     |                                |                              |
| ------------------------------------ | ---------------- | ---------------- |
| ==doc====ument.createElement('元素名');== | 创建新的元素节点 ||
| ==document.createAttribute('属性名');== | 创建新的属性节点 ||
| ==document.createTextNode('文本内容');== | 创建新的文本节点 ||
| document.createComment('注释节点');  | 创建新的注释节点 ||
|     |                                |                              |
| ==parent.appendChild( element/txt/comment/fragment );== | 向父节点的最后一个子节点后追加新节点 ||
| ==parent.insertBefore( newChild, existingChild );== | 向父节点的某个特定子节点之前插入新节点 ||
| element.setAttributeNode( attributeName );             | 给元素增加属性节点                     ||
| element.setAttribute( attributeName, attributeValue ); | 给元素增加指定属性，并设定属性值       ||



## DOM的删除节点
|     |                                |                              |
| ------------------------------------ | ---------------- | ---------------- |
| ==parentNode.removeChild( existingChild );== | 删除已有的子节点，返回值为删除节点 ||
| element.removeAttribute('属性名');   | 删除具有指定属性名称的属性，无返回值 ||
| element.removeAttributeNode( attrNode ); | 删除指定属性，返回值为删除的属性 ||



## DOM的修改节点
|     |                                |                              |
| ------------------------------------ | ---------------- | ---------------- |
| ==parentNode.replaceChild( newChild, existingChild );== | 用新节点替换父节点中已有的子节点                   ||
| element.setAttributeNode( attributeName );             | 若原元素已有该节点，此操作能达到修改该属性值的目的 ||
| element.setAttribute( attributeName, attributeValue ); | 若原元素已有该节点，此操作能达到修改该属性值的目   ||



## DOM事件

onclick事件---当用户点击时执行

onload事件---当用户进入时执行

onunload事件---用用户离开时执行

onmouseover事件---当用户鼠标指针移入时执行

onmouseout事件---当用户鼠标指针移出时执行

onmousedown事件---当用户鼠标摁下时执行

onmouseup事件---当用户鼠标松开时执行



<!--DOM事件与监听事件不是一个概念-->

<!--IE监听方法中事件类型和标准DOM监听方法中的事件类型写法有点不同，-->

<!--前者事件类型用“on”开头，例如：“onclick”、“onmousemove”等，而后者不需要“on”，就是“click”、“mousemove”等。-->