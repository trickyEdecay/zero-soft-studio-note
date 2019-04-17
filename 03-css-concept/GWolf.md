| 伪类选择器  | 作用 |
| :-: |:-: |
| hover | 设置鼠标悬浮在某一元素时的样式 |
|active|设置鼠标点击某一元素时的样式，active标签需在hover标签后设计|
|link|设置为访问过的网页链接的样式|
|visited|设置已访问过的网页链接的样式，visited标签需在visited标签后设计|
|focus|设置获得焦点时的样式 focus样式需在hover和active之前设置|
|first-child|设置父级元素中的第一个子元素的样式|
|last-child|设置父级元素中的最后一个子元素的样式|
|first-of-type|设置父级元素中的子元素第一次出现的样式|
|last-of-type|设置父级元素中的子元素最后一次出现的样式|
|nth-of-type（n）|设置父级元素中第n个子元素的样式|
>:focus->:hover->:active
>:hover->:active
>nth-of-type(2n+1)为设置序列号为奇数的子元素样式
>nth-of-type(2n)为设置序列号为偶数的子元素样式

## 1. 替换元素和不可替换元素
替换元素:浏览器根据元素的标签和属性，来决定元素的具体显示内容
不可替换元素：大多数元素为不可替换元素，内容直接表现给用户端
## 2. normal flow 
又称文档流 块级元素自上而下/行内元素在每行中自左向右依次排放顺序
## 3. 去除行内块之间的空格
行内块之间不要留空格，比如在两个行内块之间添加空的便签，添加注释
设置父级font-size:0，再设置子元素font-size
设置负外边距
## 4. vertical-align: baseline/bottom/top/middle;
使行内元素的baseline/bottom/top/middle对齐基准元素(取行高最高的作为基准)的基线
>行高为两条准线之间的距离，行距为上一个文本框基线与下一个文本框顶线的距离
## 5.行内元素与块状元素
行内元素设置上下边距、设置宽高均无效
行内元素不能包含块级元素，块级元素可以包含所有元素
相邻的兄弟块级元素、父元素和子元素会发生外边距的合并、塌陷、折叠 overflow float position inline-block
inline-block拥有block元素可设置宽高，又保持inline元素不换行的特性
## 6.position
：relative 生成相对定位元素,元素所占据的文档流位置不变，相对文档流进行偏移
：absolute 生成绝对定位元素，相对于static定位以外第一个父元素进行定位
：fixed 生成绝对定位元素，相对于浏览器窗口进行定位
：static 默认值，没有定位，元素出现在正常的流中
## 7.float 
浮动使得行内元素变为块级元素；
浮动元素脱离文档流，但是依然占据文档的空间
浮动会造成父元素塌陷及其他元素异位
## 8.overflow 
用于控制内容溢出时的处理方式 属性值有visible、hidden、scroll、auto
```css
 overflow: hidden;
 white-space: nowrap;
 text-overflow: ellipsis;
```
> 用于设置超出当行文本的内容在该行以省略号显示
>正文字体一般为14px-16px,注释-2px 
>overflow:不为visible;  float:不为none;   position:absolute/fixed;  display为inline-block,table-cell,table-caption,inline-flex会产生bfc(Block formatting context) 
>bfc为一个独立容器，容器里的子元素不会影响到外面的元素
