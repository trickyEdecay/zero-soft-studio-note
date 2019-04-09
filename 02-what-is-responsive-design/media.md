# media 媒体查询  
作用：用于页面的相应式设计，根据手机屏幕调整css的样式  
格式：@media only screen and （min-width：100px）and （max-width：640px）{  
...  
}  

样式应用范围：只对屏幕设备有效（only screen）  
屏幕宽度在大于100px且小于640px时  
将网页划为三段不同的样式：  
1. 0px-768px：手机显示器  
2. 768px-992px：ipad显示器  
3. 大于992：桌面显示器  
