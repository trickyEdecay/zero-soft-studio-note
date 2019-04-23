# git的使用

## 初始化

`$ git init`
在所在目录生成`.git`文件，所在的目录为工作区（不包括.git），.git里包括master区和stay区

## 初始配置

```bash
$git config --global user.name"YOURNAME" 
$git config --global user.email"YOUREMAIL" 
```
配置全局变量，本机所有版本的作者都是该人。

## 添加文件到版本库

```bash
git add <fileName>
......
git commit -m ["版本描述"]
```
## 版本穿梭

* 查看创库状态
  1. ` $ git status `  查看创库状态
  2. ` $ git diff `  查看修改了什么内容
* 查看版本提交日志
  1. ` $ git log ` 查看有几个版本提交到git仓库 
  2. ` $ git relog ` 查看每一次操作
* 版本回退
  1. `$ git -hard head^` 跳到上一个版本 head^^^^……最多跳到前100个
  2. `$ git -hard <fileId> `跳到指定版本
## 撤销修改

` $ git checkout --file `  可以丢弃工作区的修改

## 删除文件

` $ git rm <文件名> ` 命令git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。

## 使用远程仓库

* 创建ssh key 
  1. `$ ssh-keygen -t rsa -C "youremail@example.com"` 如果一切顺利的话，可以在用户主目录里找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人。
  2. 登陆GitHub，打开“Account settings”，“SSH Keys”页面：github的setting里添加ssh key 将id_rsa.pub的信息复制到github上添加一个个人key
* GitHub创建空仓库
  首先，登陆GitHub，然后，在右上角找到“Create a new repo”按钮，创建一个新的仓库：
  在Repository name填入learngit，其他保持默认设置，点击“Create repository”按钮，就成功地创建了一个新的Git仓库
* `git remote add origin git@github.com:michaelliao/learngit.git` 关联远程仓库
* `$ git push -u origin master` 第一次 push
* `$ git clone git@github.com:YourLink.git` 远程仓库克隆

## 分支管理

* `$ git checkout -b <dev> ` 创建并跳到分支
* `$ git branch` 查看当前分支
* `$ git checkout <分支名>` 切换到指定的分支
* `$ git merge <dev>` 合并分区
* `$ git branch -d dev` 删除分区 //强制删除用 `-D`

-* git有个最佳实践，master是主分支，用来做正式发布版之后的保留历史，其他分支包括dev用来做正常开发，多个feature用来做某些特性功能，release用来做发布版历史，每次发布都是用release打包，hotfix用来做发布版之后的一些及时迭代修复bug的工作。

## 推送分支

* `$ git remote origin`查看远程仓库分支情况，远程仓库的默认名称是origin。
*  `git push origin <分支名>`分支名可填master、、、