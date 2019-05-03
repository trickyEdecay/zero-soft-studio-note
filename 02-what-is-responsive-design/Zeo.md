# 什么是响应式设计

响应式网站设计：用自己的话理解，那就是网页（页面）有能力去自动响应用户的设备环境。

也就意味着一个网站能够兼容多个终端，而不是为每个终端都做一个特定的版本，这样，我们就不用挨个为新的设备做专门的版本设计和开发了。（**我理解为自适应网页布局大小，不知道对不对**）

## 技术实现：

按等比例缩放图片，同时保证图文混排的形式不能乱序。

①：(rwd-images.js)

②：(.htaccess)

rwd-images.js  检测当前设备的屏幕分辨率

.htaccess  决定是输出原始图片大小还是小尺寸的“响应式图片”，并进行相应的反馈输出

一些响应式设计元素如：

​     **UIKit**、**Bootstrap**、**Adobe Edge Inspect**、**Foundation**、**SimpleGrid**、**Responsive Testing**  

​           等是现成可供使用的。

**也可用一些现成的开发框架自适应响应式设计**

**Gumby Framework**、**Get UI Kit**、**Foundation**、**Semantic**、**52Framework**、**PureCSS**

**Responsablecss**、**TukTuk**、**Kube**、**Ivory**

**可用测试工具检测响应式布局设计**

​	与上述部分响应式设计框架相对应。

eg：测试工具---->**Retina Images**

Retina Images主要用来测试图片在不同的设备上的显示情况，这样有利于用户在开发出高清晰度的图片。此外，你无需更改任何img标签，并且Retina Images安装也十分方便。

​													---Fetch from baidu

​														---Rewritten by Zero-zh(曾浩)