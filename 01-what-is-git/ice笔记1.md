# 三种软件的部分快捷键
| 操作                     | sublime text   | vs code       | php storm                                    |
| :----------------------- | -------------- | ------------- | -------------------------------------------- |
| 上下移动行               | ctrl+shift+↑/↓ | Alt+↑/↓       | ctrl+shift+↑/↓                               |
| 复制行                   | ctrl+shift+d   | shift+Alt+↑/↓ | ctrl+d                                       |
| 多光标编辑               | ctrl+alt+↑/↓   | ctrl+Alt+↑/↓  | alt+想编辑的地方                             |
| 注释/取消注释            | ctrl+/         | ctrl+/        | ctrl+/                                       |
| tab/取消tab              | ctrl+] / [     | ctrl+] / [    | tab                                          |
| 查找、替换               | ctrl+f/ctrl+h  | ctrl+f/ctrl+h | ctrl+f/ctrl+r                                |
| tabsize的设置            | tabsize        | tabsize       | File -> Setting ->Editor-> Code Style -> PHP |
| 打开编辑器的插件运行列表 | ctrl+shift+p   | ctrl+shift+p  | ctrl+shift+a                                 |



# git 指令

###  配置个人信息  
> 修改个人信息和邮箱  
``` 
git config  --global user.name ["user name"]                                 
git config  --global user.email  [user email]   
```
>[]为可选项,以下同理

### 从远程下载一个文件  
```
git clone <url>
```
><>为必选项，以下同理
>url为文件地址 

### 查看文件状态
~~~
git status
~~~

### 上传文件
~~~
git init 
git add [index.html]
git commit -m "你自己的话"
git remote add origin https://github.com/Tony/vs-.git
git push -u origin master
~~~
> git init  在初始化本地仓库  
>git add 添加一个文件到缓冲区，[index.html]为文件名  
>git commit 把文件添加到本地仓库同时可以加上备注  
>git remote add 添加一个新的远程仓库，Tony为本人账户名  
>git push 将文件推送到远程仓库副本  
>origin  远程主机名，此处master为本地分支名  

==若文件被修改为新版本，但在下载了旧版本的情况下，应在上传文件前添加以下两句代码==

```
git fetch origin master
git merge master
```
>git fetch  将远程代码更新到本地仓库，此处master为远程分支名  
>git merge 合并分支，此处master为要合并的分支名  

### 查看版本和回退版本
~~~
git log [-oneline]
git reflog
git reset --hard <version num>
~~~
>git log  显示所有提交过的版本信息,oneline 是指一行显示,更加简明  
>git reflog 查看所有分支的所有操作记录  
>git reset  回退版本，后面加版本号  

### 新建或切换分支名
```
git branch <新建的分支名>
git checkout <要切换的分支名>
git checkout -b <新建并切换的分支名>
```




