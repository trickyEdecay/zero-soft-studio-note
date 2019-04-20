## Git Operate
#### 1. 配置个人信息（用户名和邮箱)
##### git config:
```bash
git config [--global] <user.name> "用户名"
git config [--global] <user.email> 邮箱
```
#### 2. 克隆远程仓库
```bash
git clone <url>
```
#### 3. 显示状态信息
```bash
git status
```
#### 4. 添加修改文件到缓冲区
```bash
git add [修改过的文件名] [-A]
```
#### 5. 提交缓冲区文件到本地仓库
```bash
git commit [-m <"修改的内容解释">]
```
#### 6. 查看版本信息（历史提交信息）
```bash
 git log [--oneline]
```
#### 7. 回滚到某一版本
```bash
 git reset [--hard] <versioncode>
```
   - hard:彻底回滚到某一版本
   - soft:回滚到某一版本，只回滚了commit的信息
#### 8. 查看操作记录
```bash
git reflog
```
#### 9. 初始化（在当前目录下生成一个隐藏的.git文件）
```bash
git init
```
#### 10. 添加远程仓库
```bash
git remote add <远程主机名,origin> <url>
```
#### 11. 将本地分支推送到远程主机
```bash
git push -u <远程主机名> <本地分支名> [:<远程分支名>]
```
#### 12. 新建分支
```bash
git branch <新建分支名>
```
#### 13. 切换到某一分支
```bash
git checkout <要切换的分支名>
```
#### 14. 新建分支并切换到此分支
```bash
git checkout -b <创建并切换的分支名>
```
#### 15. 获得远程仓库副本
```bash
git fetch <远程主机名> <远程分支名>
```
#### 16. 分支的合并
```bash
git merge <要合并的分支>
```



#### 总结：

##### 新建项目步骤：

1. 在本地工作目录下新建文件夹
2. 打开命令窗口，初始化当前目录
```bash
git init
```
3. 添加远程仓库
```bash
git remote add <远程主机名,origin> <url>
```
4. 将本地分支推送到远程主机
```bash
git push -u <远程主机名> <本地分支名> [:<远程分支名>]
```

##### 提交更新到本地仓库步骤：

1. 提交前可以先检查修改了什么内容
```bash
git status
```
2. 将想要提交的添加到缓冲区
```bash
git add [修改过的文件名] [-A]
```
3. 提交到本地仓库
```bash
git commit [-m <"修改的内容解释">]
```

##### 将本地仓库数据提交到远程仓库步骤：
1. 可先从远程仓库抓取数据（因为可能被修改过）
```bash
git fetch <远程主机名> <远程分支名>
```
2. 将获取到的远程仓库副本与本地仓库数据合并
```bash
git merge <要合并的分支（即获取的远程仓库副本分支）>
```
3. 将合并后的数据提交到本地仓库
4. 推送数据到远程仓库
```bash
git push -u <远程主机名> <本地分支名> [:<远程分支名>]
```
##### 新建分支并切换到该分支的两种写法：
1. 先新建分支，再切换
```bash
git branch <新建分支名>
git checkout <要切换的分支名>
```
2. 新建并切换
```bash
git checkout -b <创建并切换的分支名>
```
