# git基本操作
## （<>代表必须存在的内容，[]代表非必须存在的内容）
#### 1. git config //为git配置变量
- --[global] user. name <"jean"> //配置用户名
- --[global] user. email <"810438608@qq.com"> //配置 用户邮件地址
### 2. git clone  //克隆文件
语法：git clone <url>     // url 是代表克隆文件的地址 如：git clone  http://ma.sm/11.jpg
#### 3. git status  //查看git仓库的状态，例如是否有文件的修改或者其他内容的改变
#### 4. git log  //查看在git中提交的历史情况
git log  --[oneline]  //查看提交的历史情况，输出一行
#### 5.  git add [文件名] [-A]   \\将创建或者修改的文件添加到缓冲区，相当于购物时加入购物车
#### 6. git commit[-m<更新原因>] \\将缓冲区的文件上传到本地仓库，相当于将购物车的东西下单
#### 7. git reset[--hard] <versionnumber> \\退回修改前的任意版本
#### 8.git branch<新建分支名> \\ 创建分支
#### 9.git checkout -b <新建> \\ 切换到所创建的分支
#### 10. git init //初始化 
#### 11. git remote add < 远程主机的名字origin><url>  连接本地仓库与远程仓库
#### 12. git push -u <远程主机的名字> <本地分支的名字  master>：<[远程分支名]> // 将本地仓库的分支推送到远程仓库的分支上
#### 13. git merge origin //合并文件

|      操作      |  subline Text  |     vs Code      |   phpstorm    |
| :--------: | :----------: | :------------: | :---------: |
|     上下移动     | ctrl+shift+上下键 |       上下键        |      上下键      |
|     复制行      |  ctrl+shitf+D  | shit+art+up/dwon |    ctrl+D     |
|    多光标编辑     |   ctrl+鼠标右键    |     art+鼠标右键     |   ctrl+鼠标右键   |
|   注释/取消注释    |     ctrl+/ 、ctrl+u    |      ctrl+/      |    ctrl+/     |
|  tab/取消tab   | tab/shift+tab  |  tab/shift+tab   |      tab      |
|    查找/替换     | ctrl+F/ctrl+H  |  ctrl+F/ctrl+H   | ctrl+f/ctrl+R |
|  tabsize设置   |   右下角SIZE设置    |   ctrl+shift+X   |      安装       |
| 打开编辑器的插件运行列表 |  ctrl+shift+P  |      点击页面图标      | ctrl+shift+A  |