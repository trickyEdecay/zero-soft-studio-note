# 选择器
## 标签选择器
##### 作用：根据指定的标签名，在当前界面中找到所有该名称的标签，然后设置属性。
##### 格式：标签名{属性：值；}
##### 注意点：
1. 标签选择器选定的是当前界面中所有该名称的标签，而不能单独选定某一标签；
2. 标签选择器无论标签藏得多深都能找到；
3. 只要是HTML中的标签都可以作为标签选择器。
## id选择器	
##### id选择器
##### 作用：根据指定的id名称找到对应的标签，然后设置属性。
##### 格式：#id{属性：值；}
##### 注意点：
1. 每一个HTML标签都有id属性，也就是说每个标签都可以设置id；
2. 在同一个界面中id是不可重复的；
3. 在编写id选择器的时候id前一定要加#；
4. id的名称是有一定的规范的。
* 1. id的名称只能有字母、数字、下划线组成；
* 2. id名不能以数字开头；
* 3. id名不能是关键字；
* 4. 在企业开发中一般如果仅仅是为了设置样式，我们不会使用id，应为id是为了给js使用的。
## 类别选择器
##### 作用：根据指定的类名称找到对应的标签，然后设置属性。
##### 格式：.类名{属性：值；}
##### 注意点：
1. 每一个HTML标签都有class属性，也就是说每个标签都可以设置class；
2. 在同一个界面中class是不可重复的；
3. 在编写id选择器的时候class前一定要加.；
4. 类名的命名规范和id命名规范是一样的；
5. 类名就是专门给某个特定的标签设置样式的；
6. 在HTML中每个标签都可以同时绑定多个类名。
* 1. 格式：<标签名称 class="类名1 类名2 ...">
##### 确定文件当前处于什么状态
# 层次选择器
## 后代选择器
##### 作用：找到指定标签的所有后代标签，设置属性。
##### 格式：标签名称1 标签名称2{属性：值；}
##### 先找名称是标签名称1的标签，然后在这个标签下面找到名称是标签名称2的标签，然后再设置属性。
## 子选择器
##### 作用：找到指定标签的所有特定直接子元素，设置属性。
##### 格式：标签名称1>标签名称2{属性：值；}
##### 注意点：
1. 子元素选择器只查找儿子，不查找其他嵌套的标签；
2. 子元素选择器两个标签之间使用>来连接；
3. 子元素选择器不仅可以使用标签，还可以使用其他选择器；
4. 子元素选择器可以通过>一直延续下去。
##### 后代选择器和子选择器的相同点及不同点
##### 相同：
1. 子元素选择器和后代选择器都可以使用 标签名、类名、id名称来作为选择器；
2. 后代选择器和子元素选择器都可以通过空格和>一直延续下去。
##### 不同：
1. 后代选择器用空格连接；
2. 子元素选择器用>连接。
3. 后代选择器会指定后代标签中所有的特定后代标签；
4. 子元素选择器只会选中指定标签中所有直接的子元素。
## 动态伪类选择器
##### 动态伪类选择器:
1. :link	   			链接伪类选择器，超链接点击之前的状态  
2. :visited 			链接伪类选择器，超链接点击之后的状态 
##### 前面两种只用于超链接
1. :active   			用户行为选择器，点击某个标签没有松鼠标时的状态
2. :hover    			用户行为选择器，鼠标放到某个标签上的时候
3. :focus    			用户行为选择器，	获取焦点
##### 后面三种适用于所有标签(love hat) 
## 结构伪类选择器
1. .a span:first-child{  color:red;        }
##### a类元素里面第一个元素设置为红色
2. .a span:last-child{  color:red;        }
##### a类元素里面最后一个元素设置为红色
3. li:nth-of-type(n){ 属性(颜色)	}
##### 决定第n行颜色
4. li:nth-of-type(n):hover{          属性(颜色)}
##### /*效果叠加*/决定第n行颜色,光标所至处颜色发生改变
5. .a h1:first of-type{	 color:red;	}
##### 父元素中h1出现的第一次设置为红色
6. .a h1:last of-type{	color:red;        }
##### 父元素中h1出现的第一次设置为红色
****
# < input >标签 
##### 根据不同的 type 属性值，输入字段拥有很多种形式。输入字段可以是文本字段、复选框、掩码后的文本控件、单选按钮、按钮等等。
## < input placeholder=" ">  
##### 规定帮助用户填写输入字段的提示。
## < input type="button">-->
##### 定义可点击按钮
## < input type="password" value="登陆">
##### 定义密码字段。该字段中的字符被掩码。
## < input type="radio">
##### 定义单选按钮。
## < input type="checkbox">
##### 定义复选框。
****
# margin
#####  设置所有外边距属性
****
# padding
#####  设置所有内边距属性
****
# span
##### 对同一个 < span > 元素应用 class 或 id 属性
##### 例如：
##### HTML:
##### < p class="tip">< span>提示：< /span>... ... ...< /p>
##### CSS:
##### p.tip span {
##### 	font-weight:bold;
##### 	color:#ff9955;
##### }
****
##### div占用的位置是一行，
##### span占用的是内容有多宽就占用多宽的空间距离
****
# div
##### < div> 是一个块级元素。这意味着它的内容自动地开始一个新行
##### < div align="center">  居中对齐内容  < /div>
##### < div align="center">  左对齐内容   < /div>
##### < div align="center"> 右对齐内容   < /div>
****
# text-align:center;
## div{ text-align:left }   	
##### div标签对象内内容（图片和文字等）将靠左对齐
## div{ text-align:right}   	
##### div标签对象内内容（图片和文字等）将靠右对齐
## div{ text-align:center } 	
##### div标签对象内内容（图片和文字等）将居中对齐
****
# text-align:center;
##### 文本居中对齐
##### text 文本 align 对齐 centenr 中心  就是把你的文字之类的放在中间 一般用在标题里  
##### 如： < h1 style="text-align:center>标题< /h1> 
****
# border-radius:-px;
##### 圆角
****
# line-height:-px;     		
##### line-height设置内容（图片、文字）行高上下居中样式效果
****
# display:inline-block;
##### 列变行
****
# display: flex;     			
##### 换行,没它默认从上往下排列，因为它是块级元素
****
## display:inline-block;    	 
##### 外边距不塌陷
## overflow:hidden 		 
##### 外边距不塌陷，把超出的内容截掉
## float：left;			        
##### 不塌陷
## position:absolut/fixde;		
##### 不塌陷
****
# display:block；
#####  此元素将显示为块级元素，此元素前后会带有换行符。
****
# overflow
## overflow:hidden；
##### 隐藏最大高度显示溢出的内容。
## overflow:auto；
##### 如果内容被修剪，则浏览器会显示滚动条以便查看其余的内容。
## overflow:scrul;			
##### 出现滚动条
## overflow:visible;		
##### 默认值，不做处理
****
# outline-style
## outline-none 
##### 默认。定义无轮廓。 
##### 属性用于设置元素的整个轮廓的样式。样式不能是 none，否则轮廓不会出现。 
****
# inline、block			
##### 无视行内元素不能设置宽高
##### display：block将元素显示为块级元素，从而可以更好地操控元素的宽高，以及内外边距，每一个块级元素都是从新的一行开始。
##### display : inline将元素显示为行内元素，高度，行高以及底边距不可改变，高度就是内容文字或者图片的宽度，不可以改变。多个相邻的行内元素排在同一行里，知道页面一行排列不下，才会换新的一行。
##### display：inline-block看上去值名inline-block是一个混合产物，实际上确是如此，将元素显示为行内块状元素，设置该属性后，其他的行内块级元素会排列在同一行。比如我们li元素一个inline-block，使其既有block的宽度高度特性，又有inline的同行特性，在同一行内有不同高度内容的元素时，通常要设置对齐方式如vertical-align: top;来使元素顶部对齐。
****
## border:-px inset 颜色;	
##### 边宽设置，分别为：边框厚度  边框虚实线 边框颜色  
## border style:solid;
##### 设置元素所有边框的样式,或者单独地为各边设置边框样式
****
# box-sizing:
****
## letter/work-spacing:-px；
##### 字符/单词间隔
##### 字体一般大小为12px、14px
****
## text-decoration:underline
##### 定义文本下的一条线。
****
## text-index:-px；			
##### 文本缩进
****
## min  heigth: -px；
##### 最小高度，避免出现盒子里面的对象没有内容时撑不起来的情况。
## max   height:-px；
##### 最大高度，避免出现内容太多撑太高而影响美观的情况。
****
## mix width:-px；
## max width:-px；
##### 通常用于设置图片最小最大限制。当图片宽度大于最小宽度时，图片将被缩小至最小宽度；当图片小于最大宽度时，图片将被放大到最大宽度。
****
##### < h1>自带margin< /h1>
****
# white-space:
## white-space:nowrap;		
##### 不换行
## white-space:pre;		
##### 保留空格
## white-space:pre-warp;
##### 保留空白符序列，但是正常地进行换行。
****
## tabindex
##### 规定元素的 tab 键控制次序（当 tab 键用于导航时）
****
# float
## float：left;
##### 靠左浮动 (列变行)
## float: right;
##### 靠左浮动
## float: none;
##### 不使用浮动
****
# verical-align:
## vertical-align:buttom;		
##### 基线底部对齐
## vertical-slign:middle;		
##### 基线中间对齐
## vertical-align: top;  		  
##### 基线顶部对齐
## vertical-align: baseline;      	
##### 基线默认对齐 
****
## opacity:0;
##### 透明度设置为0，不仅使得元素的背景透明，连其子元素和内容都会变透明。
## background:transparent;
##### 背景色设置为transparent，只会是元素的背景色为透明的，元素里面的其他元素或内容都没有影响；
*****
# position
## position:fixed:
##### 生成绝对定位的元素，相对于浏览器窗口进行定位。
## position: static;
##### 默认值
## position: absolute;       	
##### 生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。使a元素脱离文档流（即不再安从上到上，从左到右）了
## position: relative;
##### 生成相对定位的元素，相对于其正常位置进行定位。
****
## text-overflow: ellipsis;
##### 显示省略符号来代表被修剪的文本。
****
# flex-direction:
## flex-direction: column;       
##### 横向改变的是宽度，纵向改变的是高度
## flex-direction: column-reverse; 	
##### 从下到上
## flex-direction: row;                	
##### 默认从左到右
## flex-direction: row-reverse;      	
##### 从右到左
****
# flex-wrap:
## flex-wrap: nowrap;      		
##### 默认满了也不换行
## flex-wrap: wrap;         		
##### 满了换行
****
# flex-basis:
## flex-basis: 40px;		
##### 宽40px	
###### width: 40px;				和上面的效果一样的
## flex-basis: auto;			
##### 默认值
****
## flex-shrink: 1;			
##### 默认值,收缩;;0为不收缩,012是比例数,按比例缩放
****
# flex-grow:
## flex-grow: 1;
## flex-grow: 0;				
##### 默认值（一个数字，规定项目将相对于其他灵活的项目进行扩展的量。默认值是 0。）
######	flex:0 1 auto;		
######   flex-grow: 0;		
######   flex-shrink: 1;	 
###### 三个默认值的简写	
****
# justify-content:
## justify-content: flex-start;		
##### 默认值,默认左对齐
## justify-content: flex-end;                     		 
##### 右对齐
## justify-content: center;    		
##### 控制主轴上的元素居中排序居中对齐
## justify-content: space-between;	
##### 项目位于各行之间留有空白的容器内。
****
# align-items:
## align-items: flex-start;  		
##### 交叉轴上到下
## align-items: flex-end;    		
##### 交叉轴下到上
## align-items:center;			
##### 纵向居中
## align-items: 				
##### 子元素没设置高度，会拉伸和父元素一样大;
## align-items: stretch;		
##### 默认值，元素被拉伸以适应容器，但仍遵循min/max-width/height属性的限制
## align-items: baseline;		
##### 基线对齐，少用
****
# align-content:
## align-content: flex-start;		
##### 元素位于容器的开头。
## align-content: flex-end;	
##### 元素位于容器的结尾。	
## align-content: center;		
##### 元素位于容器的中心。
## align-content: stretch;		
##### 默认值（拉伸以适应容器）
****