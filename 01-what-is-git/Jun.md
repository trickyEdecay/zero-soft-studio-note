#### 1.把项目从网上克隆到本地
>git clone < url >

#### 2.在当前项目下创建一个本地仓库
>git init

#### 3.查看该项目是否有文件被修改但未更新版本
>git status

#### 4.将项目中修改的文件加入到缓冲区
>git add [项目名称] [-A]

#### 5.将缓冲区的文件取出变成项目的新版本
>git commit [-m "备注的话"]

#### 6.查看项目的更新日志
>1.git log 查看历史所有版本信息
2.git log -x 查看最新的x个版本信息
3.git log -x filename查看某个文件filename最新的x个版本信息（需要进入该文件所在目录）
4.git log --pretty=oneline查看历史所有版本信息，只包含版本号和记录描述

#### 7.回滚历史项目
>1.git reset --hard HEAD^，回滚到上个版本
2.git reset --hard HEAD^~2，回滚到前两个版本
3.git reset --hard xxx(版本号或版本号前几位)，回滚到指定版本号，如果是版本号前几位，git会自动寻找匹配的版本号
4.git reset --hard xxx(版本号或版本号前几位) filename，回滚某个文件到指定版本号（需要进入该文件所在目录）

#### 8.连接远程仓库
>git remote add <远程主机的名字> <url>





