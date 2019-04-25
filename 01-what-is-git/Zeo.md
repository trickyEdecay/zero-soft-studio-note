# Github网页中实现团队开发的代码共享

1、      下载Git软件（百度搜索），安装

项目机主创建项目文件、添加项目文件、并且添加项目同事。

2、      打开cmd，首次打开时需要配置用户名和邮箱

eg :  git config –global user.name “Zero-zh”

  git config –global user.email [664827065@qq.com](mailto:664827065@qq.com)

3、      创建Git仓库

--先用cd命令更改路径，路径为你要clone同事的代码到什么位置

--用git init 创建Git仓库，即生成一个.git文件夹

4、获得Git仓库

​    即将Github上面同事的代码（称为远程仓库）克隆到本地仓库

​    git clone url；

5、      更改同事代码并提交

 

如在同事文件夹中添加1.c文件

先创建文件1.c

先用git status查看文件是否产生变化

git add 1.c(1.c为有更改的文件，类似于淘宝中的添加到购物车)，

git commit -m “加个备注，相当于淘宝的付款”

（可查看提交的历史记录）

git log –oneline，

然后可用git reset --adwdde(版本号)进行版本回退

6、      上传代码至远程服务器

git push origin master

7、      合并代码到作者（在本地远程仓库不用在Github同步）

打开Github网页，此项目处的new pull request，按照步骤合并，即可实现代码共享。

**看图：**

****

 ![7](C:\Users\Shinelon\Desktop\Github\7.png)

![8](C:\Users\Shinelon\Desktop\Github\8.png)

![9](C:\Users\Shinelon\Desktop\Github\9.png)

![1](C:\Users\Shinelon\Desktop\Github\1.png)

![2](C:\Users\Shinelon\Desktop\Github\2.png)

![3](C:\Users\Shinelon\Desktop\Github\3.png)

![4](C:\Users\Shinelon\Desktop\Github\4.png)

![5](C:\Users\Shinelon\Desktop\Github\5.png)

![6](C:\Users\Shinelon\Desktop\Github\6.png)

​    **机主创建远程仓库步骤：**

![11](C:\Users\Shinelon\Desktop\Github\11.png)

![12](C:\Users\Shinelon\Desktop\Github\12.png)

![13](C:\Users\Shinelon\Desktop\Github\13.png)

![10](C:\Users\Shinelon\Desktop\Github\10.png)

**创建完成，就开始上面1—7的步骤吧。**