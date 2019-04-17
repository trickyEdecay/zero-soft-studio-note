## 1.快捷键		

|    操作    |  sublime text  |    vs code    |    phpstorm    |
| :--------: | :------------: | :-----------: | :------------: |
| 上下移动行 | ctrl+shift+↑/↓ |    alt+↑/↓    | ctrl+shift+↑/↓ |
|   复制行   |  ctrl+shift+D  | shift+alt+↑/↓ |     ctrl+D     |
|多光标编辑|按住ctrl+位置|按住alt+位置|按住alt+位置|
|查找/替换|ctrl+F/H|ctrl+F/H|ctrl+R|
|tabsize设置|右下角|右下角|file-setting-editer-code style|
|打开编辑器的插件运行列表|ctrl+shift+P|ctrl+shift+x|file-setting-plugin|
|注释行|ctrl+shift+/|ctrl+k+c||
|自动排版|ctrl+shift+p+Reindent|||

# 2.Git操作指南	
 ###  git config [--global] user.name <自己喜欢的id>
 ####  git config [--global] user.email <自己的邮箱>

![](https://i.loli.net/2019/03/31/5ca01dd656ad8.png)
***
 ###  git clone <url>
  在cmd上面通过链接直接拷贝文件或者整个项目 。
1. 拷贝github上项目的链接

     >![](https://i.loli.net/2019/03/31/5ca02345b8af3.png)
2. 在cmd上进行clone

     >![](https://i.loli.net/2019/03/31/5ca023a838d4f.png)
3. 检查是否下载成功

     >![](https://i.loli.net/2019/03/31/5ca024533d85c.png)    
***
 ###  git status 
git status命令用于显示工作目录和暂存区的状态。使用此命令能看到那些修改被暂存到了, 哪些没有, 哪些文件没有被Git tracked到。
> 注意：必须在项目目录里运行cmd不然会出现以下情况  
> ![ASDASD](https://i.loli.net/2019/03/31/5ca026e9d10fb.png)
> ![ASDAS](https://i.loli.net/2019/03/31/5ca026ea4c03b.png)
***
 ### git add <文件名.xx>
将文件内容添加到索引(将修改添加到暂存区)。也就是将要提交的文件的信息添加到索引库中。之后用status就能查看修改状态。
***
 ### git commit -m "新版本的标志"  
将更改记录(提交)到存储库。将索引的当前内容与描述更改的用户和日志消息一起存储在新的提交中。
****
 ### git log [--oneline]
用于显示提交日志信息。
> ![](https://i.loli.net/2019/03/31/5ca0331a3b65c.png)
****
 ### git reset [--hard] <versioncode>
重置到log目录中的一个版本
> ![](https://i.loli.net/2019/03/31/5ca0350850ee5.png)
****
 ### git push -u <origin,远程主机名> <master,本地分支名>
此操作之前要先进行add和commit，可以通过cmd命令操作，或者直接在phpstorm上面一键操作,提交修改后，要push到github上面
****
 ### git remote add origin <url> 
添加一个新的远程仓库
 ### git branch<新建的分支名>
 ### git checkout -b<新建并切换到分支名xx>
 ### git fetch (抓取) <远程主机名><远程分机名>
 ### git merge<要合并的分支>					0.0