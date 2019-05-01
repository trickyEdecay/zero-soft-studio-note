# git 的学习笔记

# git

## 设置用户信息

git config [--global] user.information <"user.name/email">

> information:name email

## 克隆文件

git clone+<url>(目标地址)

## 查看信息

git status

## 初始化

git init

## 将文件上传到缓冲区

git add [file]

## 将文件上传到本地仓库

git commit -m "更新原因"

## 连接本地与远程仓库

git remote add origin master(origin远程仓库 master 分支名)

## 将文件上传到远程主机

git push -u  <远程主机名字><本地分支名master><远程分支名>（分支名一样可以省略）

## 显示之前版本信息

git log [--oneline]

## 回到想要的那个版本

git reset --hard+版本号

## 显示用过的版本号

git reflog

## 新建分支

git branch<新建分支名>

git branch -b<新建并切换到分支名>

## 获得最新版本

git fetch origin master

## 合并文件

git merge origin/master

## 忽略文件

文件名： .gitignore

内容：  /.idea/