#### 1.git基本配置
**配置用户名及邮箱**
> git config --global user.name "Markcjh"
> git config --global user.email 1424655745@qq.com

#### 2.查看状态
**查看工作区、暂存区的状态**
>git status

#### 3.创建git仓库
**生成一个.git**
>git init

#### 4.获得git仓库
>git clone < url >

#### 5.提交更新
>git add < index.html>[-A]
>git commit [-m < "信息" >]

#### 6.提交历史查看
**查看当前工程的所有提交的日志**
>git log[--oneline]

#### 7. 远程仓库
**查看当前的远程库**
>git remote

**添加远程仓库**
>git remote add < 远程主机的名字>< 地址>

**推送数据到远程仓库**
>git push -u< 远程主机的名字>master

**从远程仓库抓取数据**
>git fetch < 远程主机名>< 远程分支名>

#### 8.git分支
>git branch< 新建的分支名>
Git checkout<要切换的分支名>
Git checkout -b
Git fetch <远程主机名><远程分支名>
Git merge <要合并的分支>