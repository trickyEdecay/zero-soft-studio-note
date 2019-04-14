## git  
### 设置名字邮箱
1. git config --global user.name<username>

2. git config --global user.email<user email>

### git clone 从github拷贝文件

1. git clone <url>

### git status 查看git文件状态（必须是clone下来的文件才能查看状态）

1. cd进入该文件

2. git status查看文件状态
## 修改文件
1. 将文件修改后保存再用git status查看一下状态   
 
2. 发现不再是显示nothing to commit, working tree clean 
 
3. git add[index.html][-A] -A表示全部，index.html表示文件名。后面不接路径表示当前目录  

4. git commit [-m “自己的话”] 对文件进行修改注释

5. 再用git status查看一下状态后显示nothing to commit, working tree clean

### git 回退原来版本

1. git log [--oneline] 打印所有修改版本（git reflog也是打印之前的版本号）

2. git reset --hard <版本号>   回退到选择的版本号

### 怎么将文件上传到github

1. 在自己的文件夹新建一个文档

2. 在远程仓库（以github为例）在github 创建一个 repository（）

3. 按照它显示的步骤输入指令即可  
（git init初始化）  
（添加一个新的远程仓库,运行 git remote add [shortname] [url]）  
（git push -u<远程主机的名字><本地分支名>）
### 修改文件后上传到好友的github
1. 先在好友的guthub账户上用git clone <url>下载git文件
2. 修改文件，然后add commit对文件进行注释
> 注意：修改同一个文件必须要有权限，在setting中的collaborators查找想给权限的好友。  

3. git fetch <远程主机名origin><远程分支名  master>  
4. git merge origin
5. 改文档
6. 再add commit 再push
## 分支的相关指令
1. git  branch -a查看全部的分支  
2. git checkout <要切换的分支名>  
3. git checkout -b <新建并切换的分支名>  