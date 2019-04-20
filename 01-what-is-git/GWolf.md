## git命令行


#### 1.git  config 
####  配置用户名及邮箱
```  
  git config [--global] [user.name] <"user.name"> 
  git config [--global] [user.email] <"user.email"> 
```

#### 2. git clone  <url>
#####  将远程的仓库克隆到本地
```
   git clone https://github.com/GWolfQAQQ/zero-soft-studio-note.git
```

####  3.初始化
```
  git init
```

####   4.查看本地仓库状态
```
 git status
```

####  5.git add
#####  将更新的文件添加到缓冲区 A代表的是all
```
 git add  <文件名>  -A 
```

#### 6.git commit
##### 保存文件到本地仓库， -m为该次提交的附加信息
```
  git commit [-m]  <"附加信息"> 
```


####  7.查看所有版本信息 
##### oneline 为显示版本的精简化信息
```
 git log  [--oneline]
```

#### 8.查看各分支的提交记录
```
 git reflog
```

####  9.git reset 
##### 回滚到某个版本
```
 git reset -hard <version>
```

####  10.添加远程仓库
#####  origin 为远程仓库名
```
   git remote add origin  <url>
```

#### 11.将文件从本地仓库上传到远程仓库
```
  git push -u <远程主机名> <本地分支名master> [: <远程分支名>] 
```

#### 12.从远程仓库获取最新版本到远程仓库副本
##### 不会自动merge
```
   git fetch origin master 
```

#### 13.新建分支   
```
 git branch <新建分支名>
```

#### 14.新建并切换到分支      
```
  git checkout -b <分支名>        
```

#### 15.合并分支
```
git merge <要合并的分支>  
```

