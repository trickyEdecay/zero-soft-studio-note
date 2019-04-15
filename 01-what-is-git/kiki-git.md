# git的学习

### 1.基本命令

（1）git config//git配置变量
```
 - --[global] user name <user name>//设置git的用户名

 - --[global] user email <user email>设置git的邮箱
```

（2）git clone //克隆文件
```
git clone <url>//在git上clone文件到本地
```
（3）git status//查看git仓库的内容

（4）git reset [--hard] <version>//退回修改前的任意版本

（5）git branch -a//查看所有分支

（6）git branch <分支名>//创建分支

（7）git checkout <分支名>//切换分支

（8）git reflog//查看最近操作

（9）git checkout -b <新的分支名>//新建并切换到新建的分支

（10）git branch//查看当前分支，'*'后的就是当前分支

（11）git merge origin//合并文件

### 2.将文件push到github上

（1）git init//初始化

（2）git add [url][-A]//把创建的文件添加到缓冲区，

（3）git commit -m <" ">//把缓冲区的文件上传到本地仓库

（4）git remote add <orgin>  <url>//连接本地仓库和远程仓库

（5）git push -u <orgin> < master>//把本地仓库的分支推送到远程仓库的分支上



