# class3：html+css

## 常用块级元素

`p h1-h6 ul ol table div form`

> 块级元素渲染时候会渲染整个块，包括没有内容的地方

## 常用行内元素

`img a input button label textarea select`

> 行内元素只渲染标签内的内容

> 使用display可以改变块级元素和行内元素的默认渲染区域

## 选择器优先级

id选择器 优先级> class 选择器> 标签选择器

## 一些标签及其属性使用注意事项

- 使用width和height渲染图片时尽量只使用其中一个属性，避免改变图片长宽比

- 尽量不要使用<center> 标签

- 除了黑色和白色，其他颜色尽量不要用最边值

  > 其他颜色极端属性值渲染效果过于low

## 伪类选择器

- x:xxx{

​    }

>  x:xxx为伪类选择器

- 比较常用的伪类选择器：

```css
x:visited{ /* 已经访问过的链接属性设置 */
    
}

x:focus{   <!-- 焦点 -->
    
}

/* ndex:使元素获得焦点 */

x xxx:first/last-child{
  /* 匹配x类下的第一个标签且为xxx */
}

x xxx:first/last-of-type{
  /* 匹配x类下的第一次出现的xxx标签 */
```

- 类选择器"嵌套"

xx:xx:aa{

}

> example:
>
> li:nth-of-type(N):aa{//li:nth-of-type:可以指定渲染特定的li标签里面的内容,N为正整数
>
> }

## 常用的属性及属性值

display：inline-block  <!-- 行内块设置 --> 

background：  <!-- 背景颜色设置 -->

width： <!-- 宽度 -->

height： <!-- 高度 -->

border-radius：<!-- 圆角 -->

text-align：center <!-- 水平居中 -->

line-height：     <!-- 竖直设置 -->

color： <!-- 字体颜色设置 -->

position： absolute   <!-- 使该标签脱离文档流-->

​                   relative     <!-- 使之以一层盒子为基准-->

​                     fixed         <!--  绝对定位 -->

white-space:nowrap <!-- 块里不换行 -->

letter-spacing:  <!-- 字距 -->

text-decoration: <!-- 下划线 --> .

overflow-x/y:auto; <!-- 自动滚动条 -->

font-size:0;<!-- 取消行内块空格 -->

text-overflow:ellipsis<!-- 单行内容省略 -->