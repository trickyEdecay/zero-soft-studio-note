#### 1.配置账户

> - ` git commit [--global] user.email<“email@qq.com”>` #设置用户名
> - `commit [--global] user.name <username>`  #设置邮箱地址(建议用注册giuhub的邮箱)

#### 2.远程克隆git项目

> - `git clone <url>`  克隆前要记得cd好克隆的位置

#### 3.查看仓库状态

> - `git status`

#### 4.将需要提交的文件放入购物车

> - `git add [index.html] [A]`

#### 5.查看版本日志

> - `git [log] [--oneline]`

#### 6.更改提交的操作

> - `git reset [---hard] <versioncode> `回溯到指定状态，只要提供目标时间点的哈希值
> - `git reset` **回溯历史版本**

#### 7.将修改提交的本地仓库

> - `git commit [-m <“版本概述”>]`

#### 8.将修改的文件上传到远程主机上

> - `git push -u <远程主机名> <本地分支名>[:<远程分支名>]`

#### 9.添加一个新的git远程仓库 <origin>作为远程主机的名字

> - `git remote add <远程主机名 （origin）>  <url>`

#### 10切换到某一分支

> - `git checkout <分支名>`切换到某个分支

#### 11建立一个新的分支 并给予命名

> - `git branch <新建立的分支名>`

#### 12 建立一个新的分支命名完切换过去

> - `git branch -b <建立新的分支名>`

#### 13 合并分支

> - `git merge<要合并的分支>`

#### 14  取回分支

>- `git fetch <远程主机名><远程分支名>`