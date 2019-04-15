# 响应式设计(css)
---
### 1. 使用@media(css中定义)  
  
##### media <类型> [and <条件>] [and <条件>]
  
**类型 :**  
* `all`运用于所有媒体类型的设备上  
* `print`只运用于打印机设备上  
* `screen`只运用于屏幕设备上（电脑，平板电脑，手机等等） 
* `speech`只运用于屏幕阅读器上  
  
### 2. 使用@import(css中定义)  
##### @import url <"文件地址"> [ <类型> and <条件>]  
  
### 3. 使用Link标签连接(写在**head**里面)  
```
<link rel="stylesheet" type="text/css" href="<css文件地址>" media="[类型] [and <条件>]">
```  

---  
 
### 条件:  
* `max-width` : 指渲染界面最大宽度,若超过,则不显示css内容  
* `min-width` : 指渲染界面最小宽度,若不超过,则不显示css内容
* `min-device-width` : 指所使用设备的最小屏幕宽度,若不超过,则不显示css内容
* `max-device-width` : 指所使用设备的最大屏幕宽度,若超过,则不显示css内容
* `min-device-height` : 定义设备输出的最小屏幕可见高度
* `max-device-height` : 定义设备输出的最大屏幕可见高度