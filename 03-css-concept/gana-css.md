# css
## 创建css
1. 使用元素内嵌样式表：不推荐使用
2. 使用文档内嵌样式表：在<head></head>里面加入<style></style>,在<style></style>里面写
3. 外部样式表：```<link href="加css文件地址" rel="stylesheet">```   
> 注意这里的link用的是href 而不是src！！！！  
> 然后后面的rel标签属性不能省略，这样子写法就是引入外部的css   
## 盒子模型content box
1. content:内容  
2. padding：填充  
3. border：边框   
4. margin：边界  
padding，margin：后面加四个数值为上、右、下、左的数值  
后面加两个表示 上下，左右 的数值  
加一个表示上下左右都是这个边距数值  
border：后面加的第一个数为边框的宽度，第二个加边框的样式类型，第三个加边框的样式   
填充background是填充content area 和 border和 padding    
所有标签都适合于盒子模型
 
## 选择器
1. 根据类选择元素使用class   .类名{}  
 在标签里class属性可填多个
  
2. 根据ID选择元素id     #id号{}    
3. 根据标签选择选择元素    
可以多个元素一起例如 h1，p{} 中间以‘，’隔开可以并几个标签   
h2 p{}后代选择器，h2里面的p标签  
h1 >span{}直属后代选择器   
> id选择器 优先级>class 选择器>标签选择器
##伪类选择器
1. hover在active（激活）上面
2. link在visited上面
3. a：link{}是在a标签内且必须是链接才能执行
4. a：visited{}是点进链接访问后执行的操作
5. focus：当元素获得焦点时的变化
6. first-child：选择第一个子标签
7. last-child：选择最后一个子标签
8. last-of-type：子标签出现的最后一个
9. first-of-type：子标签的出现第一个  
``` .a span:first-child``` a标签内出现第一个的span标签
10. nth-of-type（1）：选择第一个  
nth-of-type（n）：选择全部  
nth-of-type（2n）：选择偶数项   

```

  	li:nth-of-type(2n+1):hover{ //伪类选择器可以叠加
  		background: red
  	}
 
   	<ul>
   		<li>萝卜</li>
   		<li>玉米</li>
   		<li>生菜</li>
   		<li>番茄</li>
   	<ul>
``` 
## 块级元素与行内元素
  每一个标签都有自己默认的行为，那么我们一般管这种自己会独占一行的标签元素叫做块级元素  
管这种不会占一行的元素叫做内联元素/行内元素  
* 块级元素：p h1-h6 ul ol table div form  
* 行内元素：img a input button label textarea select  
* 外边距的合并/折叠：  
1. 相邻的兄弟块级元素之间   
2. 父块级元素和子块级元素之间（取大值）为了不使子元素漏出来，应在父元素设置border   
* 块级元素可以包含行内元素，行内元素不可以包含块级元素
行内元素不可以设置margin border的上下不可以设置左右可以设置，不可以设置宽高。但行内元素且是可替换元素可设置宽高   
外边距不会折叠的情况：  
1. 两个line-block 
2. float 绝对定位
overflow：hidden 不会影响到外面 
display：inline-block 行内块。先把行内元素弄成块级元素，然后放在所在那一行，不另起一行  
## 可替换元素，不可替换元素
img标签是可替换元素
可替换元素：想象不出来的内容都是可替换元素  
## 文档流
normal flow：正常流(文档流)，从上到下，从左到右 
position：static;默认static。代表文档流  
position:relative  
left:10px;向左偏移10px  
top:10px;  向上偏移10px
position：absolute绝对值 脱离文档流
position：fixed 固定
}
在父类设置position：relative，子元素找到父元素不是static的作为它的参考系
## 字体
1. 正文：14~16px像素 偶数值
2. 提示文：比正文小2px 
3. font-weight: 字体宽度 100-900 以百为单位
4. color：字体颜色
5. font-size：字体大小
6. text-decoration：装饰 
设置a标签的text-decoration=none可以把a的下划线去掉
7. white-space：nowrap   框内文字溢出也不会换行
8. white-space：pre;     &nbsp空格  &lt是<  &gt是>
9. text-align:center; 水平的居中对齐
10. line-height: 垂直的居中对齐
## css的一些属性
1. tabindex=“正整数”可以使一些标签获得焦点  
2. outline：none 轮廓，是绘制于元素周围的一条线，位于边框边缘的外围
3. vertical-align 属性设置元素的垂直对齐方式，该属性定义行内元素的基线相对于该元素所在行的基线的垂直对齐
##滚动条
over-flow-y:scroll;有没有溢出都有滚动条
over-flow-y:auto：溢出有滚动条，没有溢出没有滚动条
text-overflow：ellipsis；溢出显示省略的效果...应用于单行 

