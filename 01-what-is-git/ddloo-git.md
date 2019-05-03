# git笔记  
---
作者:ddloo  
 ---  
## **一. 利用git命令配置个人信息与创建git仓库** <i class = "icon-pencil"></i> 
 
### **1. git config**  

``` git
git config [--global] user.name + “username”(自己的使用的名字)  
 git config [--global] user.email + useremail(自己使用的邮箱地址)  
 ```

用以上两个命令可以配置自己的名字与邮箱。请注意，如果使用了 **--global** 选项，那么该命令只需要运行一次，因为之后无论在该系统上做任何事情， Git 都会使用那些信息。  

### **2. git clone <url>**  
  
git clone + 一个远程仓库地址,即表示为在该远程仓库中克隆全部项目文件到本地文件中,并在克隆的时候git会在当前本地文件中生成一个.git[^.git]隐藏文件夹.  

```git
git clone https://github.com/ddloo/zero.git
```  
这里的意思是 在https://github.com/ddloo/zero.git中克隆该远程仓库中的项目到自己的当前文件夹中.那如果不用 **git clone** 克隆,直接从网址进行下载,则下载的文件夹中没有 **.git** 隐藏文件夹 

### **3. git init**  

使用该命令可以在当前文件夹创建一个.git文件,将其初始化,主要用来创建git仓库.  

----  

## **二. 用git命令查看与保存、修改工作目录** <i class = "icon-pencil"></i> 

### **4. git status**  

查看工作目录(本地工作项目)中是否有内容被修改后没有 **add** 与 **commit** 。  

### **5. git add 与 git commit**  

**git add** [文件名] [-A] : **-A** 代表全部文件,此时不需要输入 `[文件名]` ,若没有 **-A** 则需要自己手动输入自己想要放入缓冲区的 `[文件名]` .  
**git commit** [-m <"这次修改的内容">] : 对在缓冲区的修改进行修饰,并将缓冲区的内容踢出去到本地仓库中修改.  

![](https://i.loli.net/2019/04/08/5cab14b65d15e.png)

对想要修改的内容**add**到缓冲区,然后**commit**到本地仓库,例如:这次更新了时间与功能,则将“更新时间”作为一个新版本**add**中缓冲区中,接着**commit**到本地仓库.然后再将"更新功能"**add**与**commit**重复一次,如此多了两个新版本:1.更新时间。2.更新了时间与功能。  

### **6. git log [--oneline]**  

查看日志,看自己之前的版本与现在的版本,方便回退版本。  

### **7. git reset**  

>**git reset** [--hard] + versioncode(想要回滚到哪个的版本号,用git log查看版本号)
>**git reset** [--soft] + versioncode  

##### --hard : 回滚到git add之前的状态  
##### --soft : 回滚到 git add 之后, git commit 之前的状态  

---  

## **三. 用git命令创建分支并向远程仓库上传新的版本**  <i class = "icon-pencil"></i>

### **8. git remote(远程) add**  

git remote add <远程主机名字> <远程主机的地址> : 创建远程主机,并为它指向远程地址,远程主机名字一般默认为 `origin`。  

### **9. git push [-u] <远程主机名字> <本地分支名>**  

1.**git push** -u origin master :  将本地的master分支推送到origin远程主机，同时指定origin为默认主机。  
2.**git push** : 将当前分支发送到默认的远程主机。  
3.**git push** origin : 将当前分支推送到origin主机分支上。  

### **10. git branch**  

**git branch** <新的分支名字> : 创建新的分支名。  

### **11. git checkout**  

```git
git checkout <想要切换的分支名>;
git checkout -b <新建一个分支名并切换到该分支>;
```  

### **12. git merge**  

**git merge** <分支名字> : 将其他分支名的内容合并进当前分支。若发现合并冲突,就需要我们手动调整冲突,哪些要留下来,哪些不要。  

![](https://i.loli.net/2019/03/31/5ca058f03f914.png)  

如图,a3与a2合并为a5,a5与a4合并为a6。  

### **13. git fetch**  

>**git fetch** <远程主机名字> <想要准备合并的分支> : 捉取远程仓库内容放在远程仓库副本,用于合并。  


[^.git]: .git文件夹是当前目录生成的一个管理git仓库(本地仓库)的文件夹,里面有git操作不可或缺的东西。