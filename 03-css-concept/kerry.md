### 特殊知识点

1. #000000  红绿蓝    不用最边角颜色，除黑白
2. 不用\<center>标签使文本居中
3. normalize.css   重置默认值
4. \>直属子标签  h2>span
5. 选择器列表     后代选择器
6. 盒子模型设置颜色的话，影响content，padding,border
7. 行高：基线与基线的距离
8. 可替换元素(想象不出来内容的,可设置宽高)   img,input         不可替换元素
9. overflow:hidden    float:right/left    position:absolute/fixed  产生bfc
10. 正文  14/16px         辅助/提示文字   正文-2
11. 转义字符
12. cale   尽可能不用

### 元素

1. 块级元素  p  h  ul ol  table  div  form              能设置宽高
2. 内联元素/行内元素   img  a input  button label textarea select  span   要设宽高，用display:inline-block
3. 行内块元素  可替代元素

### 居中

1. 文本   text-align,height-line
2. 块级    margin:0  auto

### 选择器

1. 标签选择器
2. id选择器     #
3. 类选择器     .        可设多个   class="big    small"

### 优先级

1. 外部样式表小于style标签
2. style标签小于内联样式
3. id选择器>class选择器>标签选择器
4. 多个选择器，指向越准确，优先级越高   eg:h2>span       p span
5. 优先级改变!important，不能用，用了打死你

### 属性

| 属性     | have                                                         |
| -------- | ------------------------------------------------------------ |
| 尺寸属性 | width   height                                               |
| 字体属性 | font-size  font-family:"   ","   " 第一个没有，找第二个,最后设必有字体   font-weight:100-900  整百 |
| 文本属性 | color   text-decoration:(none underline  overline line-through删除线) text-align  line-height: em     letter-spacing     word-spacing      white-space:nowrap(不换行) pre |
| 背景属性 | background-color/image/repeat/position        background     |
| 边框属性 | border-top/right/bottom/left:粗细  线型(none  solid  dashed  dotted)   颜色    border-radius:8px |
| 内边距   | padding-top/bottom/                                          |
| 外边距   | margin-top/bottom/                                           |
|          |                                                              |

| 特别属性                                                     | 注释                 |
| ------------------------------------------------------------ | -------------------- |
| display:block inline  inline-block                           | 如何显示             |
| float:right/left                                             | 浮动                 |
| outline:none;                                                | 原本框颜色变无       |
| tabindex="一个正整数"                                        | 使之可获得焦点       |
| vertical-align:bottom                                        | 以盒子的最低端为基线 |
| opacity:0-1                                                  | 设置透明度           |
| overflow(-x/y):hidden(截掉超出的)   scroll(滚动条)   auto(自动)  visible(默认) |                      |
| text-overflow:ellipsis                                       | 运用在单行           |





### 伪类选择器

| 伪类选择器                | 注释                   |
| ------------------------- | ---------------------- |
| link                      | 链接                   |
| visited                   | 被访问                 |
| hover                     | 悬浮                   |
| active                    | 点下                   |
|                           |                        |
| first-child               | 第一个子元素且标签符合 |
| first-of-type             | 第一次出现时           |
| nth-of-type(2   2n  2n-1) | 准确值  或奇偶         |
|                           |                        |
| focus                     | 获得焦点时             |



### 块级元素(盒子)

#### 盒子左右无空格的方法

1. 无转行
2. font-size
3. margin为负

#### 注意

1. 兄弟的块级元素外边距可合并
2. 父子的块级元素外边距的合并,可用border阻止
3. 块级元素沾满一行？margin-right:auto;
4. 块级元素居中：margin:0 auto;
5. vertical-align:bottom        以盒子的最低端为基线
6. box-sizing:border-box

#### position

1. static(默认)
2. relative相对
3. absolute绝对  脱离文档流 找到上级不为static的作为参考系
4. fixed固定  脱离文档流  上下滑不影响其位置

### 媒体查询

@media screen and (max-width: 300px){

}

