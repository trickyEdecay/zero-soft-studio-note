#### 响应式设计：
|       名称 |    布局    |
| ---------: | :--------: |
|     static |  静态布局  |
|      fluid |  流式布局  |
|   adaptive | 自适应布局 |
| responsive | 响应式布局 |

>对于多数网站来说，为每种**新设备及分辨率创建其独立的版本**根本就是不切实际的；结果就是，会赢得使用某些设备的用户群，而失去那些使用其他设备的用户。
>
>###### 响应式Web设计(Responsive Web design)的理念是，页面的设计与开发应当根据用户行为以及设备环境(系统平台、屏幕尺寸、屏幕定向等)进行相应的响应和调整。



##### @media的css语法：
```css
@media mediatype and|not|only (media feature) {
    CSS-Code;
}
```



##### css3支持的媒体类型：（部分已废弃的没写入）

| 值     | 描述                               |
| ------ | ---------------------------------- |
| all    | 用于所有设备                       |
| print  | 用于打印机和打印预览               |
| screen | 用于电脑屏幕，平板电脑，智能手机等 |
| speech | 应用于屏幕阅读器等发声设备         |



##### 在Media Queries 中，我们最常使用min-width 和max-width 来判断使用者的视窗宽度

##### 下面的id样式只有在浏览器或屏幕宽度超过500px时且不超过1000px才会有效：
```css
@media screen and (min-width: 500px) and (max-width: 1000px) {
    #MyID {
        width: 30%;
        float: right;
        background: pink;
		text-align: center;
    }
}
```


>**min-width**和**max-width**这两个属性很靠谱。通过**min-width**的设置，我们可以在浏览器窗口或设备屏幕宽度高于这个值的情况下，为页面指定一个特定的样式表；**max-width**则反之。



##### 下面的class类样式只有在设备本身屏幕宽度不超过480px才会有效：

```css
@media screen and (max-device-width: 480px) {
    .classForiPhoneDisplay {
        font-size: 12px;
    }
}
```

>**min-device-width**与**max-device-width**，用来判断设备本身的屏幕尺寸。



##### 下面的class类样式只有在设备横屏时才会有效

```css
@media screen and (orientation: landscape) {
    .iPadLandscape {
        width: 30%;
        float: right;
    }
}
```
>**orientation(方向)**属性尤其有用。它的值可以是**landscape(横屏)**或**portrait(竖屏)**。



##### 区分普通显示屏和高清显示屏:
```css
.css{     /* 普通显示屏(设备像素比例小于等于1.3)使用1倍的图 */ 
    background-image: url(img_1x.png);
}
@media screen and (-webkit-min-device-pixel-ratio:1.5){
.css{     /* 高清显示屏(设备像素比例大于等于1.5)使用2倍图 */
    background-image: url(img_2x.png);
  }
}
```
>**device-pixel-ratio **它是设备上物理像素和设备独立像素( device-independent pixels (dips) )的比例，即 devicePixelRatio = **屏幕物理像素/设备独立像素**；
>**例如：**iPhone4S，分辨率为：960×640，取屏幕宽度计算，物理像素640px，设备独立像素320px，那么，devicePixelRatio 值为 640px / 320px = 2，又如iPhone3，计算出来的 devicePixelRatio 值为 320px / 320px = 1





>**分辨率（resolution）**指定输出设备的分辨率（像素密度）。分辨率可以用每英寸（dpi）或每厘米（dpcm）的点数来表示
>
>**宽高比（aspect-ratio）**描述了**输出设备目标显示区域**的宽高比。该值包含两个以“/”分隔的正整数。代表了水平像素数（第一个值）与垂直像素数（第二个值）的比例
>
>**设备宽高比（device-aspect-ratio）**描述了**输出设备**的宽高比。该值包含两个以“/”分隔的正整数。代表了水平像素数（第一个值）与垂直像素数（第二个值）的比例