### 父元素设宽高200px，其中子元素设宽高为100%
1. 父元素的可分配空间是父元素的content部分；
2. 子元素的100%是父元素的content部分；
3. 父元素具有padding值时，子元素的100%是父元素的content部分；
4. 父元素设box-sizing值时，子元素的100%是父元素的content部分；
5. 子元素设box-sizing值时，子元素的100% 是父元素的content部分；
6. 子元素如果超过父元素的可分配空间，超过部分处理：在父元素用overflew：hidden或者overflew：scroll；
7. 子元素如果padding-left设为99%，width为1%，发生了子元素padding在父元素的content中撑开，子元素的content在剩下的父元素中撑开，如果父元素的content不够会和父元素的padding重合；
8. 子元素的margin跟父元素的padding子元素：margin在父元素的content中撑开。如果父元素的content不够，会与父元素的padding重合。
### 弹性布局 
      display：flex；
      flex布局以后float，clear，vertical-align属性的将失效。
 ![flex](https://i.loli.net/2019/04/18/5cb897bbf2970.png)
 容器默认存在两根轴：
 水平的主轴（main axis）和垂直的交叉轴（cross axis）。
 主轴的开始位置（与边框的交叉点）叫做main start，结束位置叫做main end；交叉轴的开始位置叫做cross start，结束位置叫做cross end
###### flex container 属性（父元素）
1. flex-direction（决定主轴方向）
    取值：row（默认左-->右）/colum（上-->下）/row-reverse(右-->左)/colum-reverse(下-->上)
2. flew-wrap(定义:如果一条轴线排不下，如何换行)
    取值：nowrap(不换行，默认挤在一起)/nowrap(换行)/nowrap-rverse(换行，第一行在下方)
3. justify-content（定义了项目在主轴上的对齐方式）
    取值：flex-start(沿着主轴左端对齐) /flex-end (沿着主轴末端对齐) / center (沿着主轴中心对齐) / space-between(沿主轴两端对齐，项目之间的间隔都相等)/ space-around（每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。）;
![justify-content](https://i.loli.net/2019/04/18/5cb89db1e800c.png)
4. align-items(定义项目在**交叉轴**上如何对齐)
> 取值：flex-start（交叉轴起点对齐） | flex-end （交叉轴末端对齐）| center（交叉轴中心对齐） | baseline（项目的第一行文字的基线对齐） | stretch（子元素不设高度时，自动拉升填满父元素）;
> 

5. align-content(定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用)
取值： flex-start | flex-end | center | space-between（与交叉轴两端对齐，轴线之间的间隔平均分布 ）| space-around | stretch（轴线占满整个交叉轴）
###### 项目的属性（子元素）
1. order：0（定义项目的排列顺序。数值越小，排列越靠前，默认为0。）
![justify-content](https://i.loli.net/2019/04/19/5cb8a051662bc.png)
2. flex-grow(定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大)
 >  flex-grow:1，等分剩余空间，不存在空隙；
 > 如果一个项目的flex-grow：2，其他项目都为1，则前者占据的剩余空间将比其他项多一倍
 > 

3. flex-shrink（项目的按缩小比例，默认为1，即如果空间不足该项目将缩小）
     flex-shrink：0，不缩放

4. flex-basis（项目在主轴上的尺寸，默认值为auto，即项目的本来大小）
    可以设为跟width或height属性一样的值（比如350px），则项目将占据固定空间

5. flex：flex-grow,flex-shrink 和 flex-basis的简写，默认值为`0 1 auto` 

6. align-self（允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。）
   align-self: auto | flex-start | flex-end | center | baseline | stretch;
 ![justify-content](https://i.loli.net/2019/04/19/5cb8a3550b7e1.png)
7. 弹性项目之下的子元素不遵循弹性布局，而是属于BTF（块级格式上下文）
