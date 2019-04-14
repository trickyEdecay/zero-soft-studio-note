[TOC]

------

# 关于Typora的使用

## 标题

#为一级标题

##为二级标题

###为三级标题

####为四级标题

#####为五级标题

######为六级标题

*注意：没有七级标题*

## 引用

【>】表示引用

多层嵌套引用可使用【>>】，以此类推

默认以引用开头，回车后仍是引用：

> 引用第一行
>
> 引用第二行
>
> > 引用内部引用第一层
> >
> > > 引用内部引用第二层

空回车即可结束引用，根据嵌套层数按回车次数

## 代码

1. 单行代码引用

​       以[单撇]开始和以[单撇]结束，这是最简单的单行代码引用：

​     `android: src="@drawable/jyu"`

2. 多行代码引用

   输入[三撇+语言名称 ```/~~~+language name]回车就会出现*代码块*:

   ```php+HTML
   int a=10;
   int b=5;
   ```

## 列表

1. 无序列表

   【*】无序列表一

   【+】无序列表二

   【-】无序列表三

   * 无序列表一

   + 无序列表二
   - 无序列表三	

   1.2 多层无序列表

   tab+* 多层无序列表：		

   * 多层无序列表1
     * 多层无序列表2
       * 多层无序列表3	

2. 有序列表

   数字序号+空格+列表内容：

   1. 有序列表1
   2. 有序列表2
   3. 有序列表3

3. 可选序列

   序列标号+空格+[ ]+空格+内容：

   - [ ] 可选序列1
   - [ ] 可选序列2

4. 任务列表（复选框）

   -+空格+[空格]+空格+内容——表示没有选中的复选框

   -+空格+[x]+空格+内容——表示选中的复选框：

   - [ ] 复选框1

   - [x] 复选框2

    ## 表格

|列名|列名|+换行键,创建一个两行两列的表格：

| 第一列 | 第二列 |
| :----- | ------ |
|        |        |

鼠标点击表格，可调整表格行列数、字体位置、删除表格等等。

## 模式

源代码模式：ctrl+/

专注模式：F8

打字机模式：F9

## 格式

1. 链接

输入<url>，按ctrl并单击该链接，即可跳转到相应页面：https://www.baidu.com

插入方法：[标题]（路径）： [百度](https://www.baidu.com/)

1.1 锚点

用来跳转到文章的指定处。

```
##0.目录{#index}
跳转到[目录](#index)
```

2. 图片

！[图片描述] （图片链接/路径）——插入图片：

！[人物](C:\Users\Dsx\Pictures\Saved Pictures\324492.jph)

也可以直接将图片拖动到指定位置或者按快捷键插入。

3. 加粗

在内容两端各加两个星号或者两个下划线：**内容**/__内容__

4. 斜体

在内容两端各加一个星号或者一个下划线：*内容*/_内容_

5. 下划线

在内容左边加<u>，右边加</u>: <u>内容</u>

6. 删除线

在内容两边各加两个代替号：~~内容~~

7. 分割线

输入三个及以上*、-或_:

***

---

___

   7.1 水平分割线

------



## *附加*

常用快捷键：

加粗——ctrl+B

斜体——ctrl+I

字体——ctrl+数字

下划线——ctrl+U

返回开头——ctrl+Home

返回结尾——ctrl+End

生成表格——ctrl+T

超链接——ctrl+K

生成目录：[TOC]+enter

选中一整行：ctrl+l

选中单词：ctrl+d

选中相同格式的文字：ctrl+e

搜索：ctrl+f

替换：ctrl+h

删除线：alt+shift+5

插入图片：ctrl+shift+i

插入代码：ctrl+shift+`

高亮显示：==高亮显示==

表情：:smile:

# git学习笔记

## git初始化及仓库创建与操作

### git config 

该命令用于获取并设置存储库或全局选项，这些变量可以控制Git的外观和操作的各个方面。

基本信息设置

1. 设置用户名

```git config [--global] user.name <user name>

```

2. 设置用户名邮箱

```git config [--global] user.email <user email>

```

3. 查看设置：`git config -list`

### git clone

目的：将远程仓库（github对应的项目）复制到本地。

`git clone <url>(仓库地址)`

*注意：<>表示必要的内容，[]表示非必要的内容*

### git add

该命令将文件内容添加到索引（将修改添加到暂存区），也就是将要提交的文件信息添加到索引库中。

git add+文件名（添加到暂存区）：

`git add [index.html] [-A]`

### git commit

该命令主要是将暂存区里的改动提交到本地的版本库。

git commit -m "提交描述"（将文件从暂存区提交到仓库）：

`git commit [-m <"message">]`

git commit -m "第一次通过git删除仓库文件"（提交删除请求）

git commit -m "第一次通过git修改文件并提交到仓库"（通过git修改文件并提交到仓库）

### git status

该命令用于显示工作目录和暂存区的状态，不显示已经被commit到项目历史中去的信息。

### git log

该命令可查看项目历史的信息。

参数可以将每条日志的输出为一行：`git log [--oneline]`

### git init

该命令可以创建一个全新的空仓库或者将已经存在的项目纳入版本管理。

创建bare(裸仓库，即没有工作仓的仓库)：`git init <--bare>`

### git branch

该命令用于列出、创建或删除分支。

git branch+新建的分支名（创建分支）：`git branch <dev>`

git branch+-d+新建分支名（删除分支）：`git branch [-d] <dev>`

### git reset

该命令用于将当前HEAD复位到指定状态，可将当前分支（branch）重置到某次提交。

git reset --hard(重置stage区和工作目录)：

`git reset [--hard] <versioncode>`

git reset --soft(保留工作目录，并把重置HEAD所带来的新差异放进暂存区)：

`git reset --soft HEAD`

git reset --mixed(保留工作目录，并清空暂存区)：

`git reset HEAD`/`git reset --mixed HEAD`

### git checkout 

该命令用于切换分支或恢复工作树文件，能重写工作区。

git checkout+要切换的分支名（将分支切换到master）：`git checkout <master>`

git checkout+-b+新建并切换到分支名（当分支不存在时，若存在只需切换分支）：`git checkout [-b] <master>`

查看帮助：`git checkout --help`

### git merge

该命令用于将两个及两个以上开发历史合并一起。

git merge+要合并的分支：`git merge dev`

### git fetch

该命令用于从另一个存储器下载对象和引用。

git fetch+远程主机名+分支名：`git fetch <origin> <master>`

更新所有分支：`git fetch`

查看远程分支：`git fetch -r`

查看所有分支：`git fetch -a`

|           操作           |  sublime text   |    vs code     |        phpstorm        |
| :----------------------: | :-------------: | :------------: | :--------------------: |
|        上下行移动        | ctrl+shift+↑\|↓ |     上下键     |    ctrl+shift+↑\|↓     |
|          复制行          |  ctrl+shift+d   | shift+alt+↑\|↓ |         ctrl+d         |
|        多光标编辑        |  ctrl+鼠标右键  |  alt+鼠标右键  |      alt+鼠标右键      |
|      注释/取消注释       |     ctrl+/      |     ctrl+/     |         ctrl+/         |
|       tab/取消tab        |  tab/shift+tab  | tab/shift+tab  |     tab/shift+tab      |
|        查找/替换         |    ctrl+f/h     |    ctrl+f/h    |         ctrl+r         |
|      tabsize的设置       |     右下角      |     右下角     | 在files>settings里面找 |
| 打开编辑器的插件运行列表 |  ctrl+shift+p   |  点击页面图标  |           /            |

