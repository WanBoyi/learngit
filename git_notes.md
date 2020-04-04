## 1. 创建版本仓库
#### 1. 通过下面的命令可以创建版本仓库
```c
$ mkdir learngit
$ cd learngit
$ pwd //用于显示当前的目录
```
会返回当前目录信息，并且在当前目录创建一个空文件

#### 2. 初始化空仓库
```c
$ git init
Initialized empty Git repository in /Users/michael/learngit/.git/
```
.git文件是用于管理仓库的，不用手动操作

#### 3. 添加文件到版本库
（这里有个坑是用windows的记事本编辑文本文件，解决方案是用notepad++或者就用.md文件）
+ 首先在当前的目录下手动创建一个readme.md文件
+ 其次使用**git add**添加文件
+ 最后使用**git commit**提交改变
>$ git commit -m "wrote a readme file"
-m后面跟的是这次操作的备注，方便以后查阅

返回的是下面的内容
```c
[master (root-commit) eaadf4e] wrote a readme file
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt
```
表示一个文件被改动，添加了两行的内容
**一次commit之前可以多次add file**

## 2. 修改文件的内容
改了文件中一行的内容（添加了一个单词）
使用**git status**查看修改情况
```c
On branch master
Changes not staged for commit://意思是修改了但没有提交
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")
```
使用**git diff readme.md**查看具体修改的细节
看过细节之后可以提交了，提交分三步
>1.git add readme.md
>2.git status
>3.git commit -m "add distributed"

之后也可以通过**git status**查看当前状态

## 3. 版本回退
回顾一下，readme有两个版本，第二个版本加了个单词，现在修改并提交第三个版本（这次对第二句进行扩充），在修改文件，git add，git commit之后，我们可以通过**git log**查看日志
```c
commit 6e19a1a092957019edf82e077b473ad803bcbfb3 (HEAD -> master)
Author: wby <wby@bupt.edu.cn>
Date:   Fri Apr 3 10:10:23 2020 +0800

    append GPL

commit 2d1aa7233568fd913dc04d3a59e89fbb8b11a57b
Author: wby <wby@bupt.edu.cn>
Date:   Fri Apr 3 00:50:50 2020 +0800

    add distributed

commit ffd02d9c800dc5eec403507dd57ca688c91648ee
Author: wby <wby@bupt.edu.cn>
Date:   Fri Apr 3 00:45:31 2020 +0800

    wrote a readme file
```
可以非常清楚的看到三次提交的时间与备注，commit后一大串的东西是版本号

好的，下一步我们需要回退到第二个版本add distributed
HEAD表示当前版本，HEAD^表示上一个版本，HEAD^^表示上两个，HEAD~100表示上一百个
使用这个命令回退一个
>$ git reset --hard HEAD^
返回结果
>HEAD is now at 2d1aa72 add distributed
表示是第二个版本了
此时查看内容
>$ cat readme.md
发现确实被还原了
使用**git log**发现第三版没有记录了，这时候可以翻到上面的log，用版本号前几位进行查找
>$git reset --hard ffd02d
Git内部通过版本指针指向不同的版本，这样回退就比较快，可以使用
>$ git reflog
查找历史上所有的命令，再通过版本ID回到任一个版本
（git log是提交历史，git reflog是命令历史）

## 4. 工作区与暂存区
工作区：learngit文件夹就是一个工作区
版本库：.git是版本库，第一个分支是master，指向master的指针叫HEAD
 
每当向工作区内的文件进行改动之后，版本库的指针也会发生改动
 
每次使用git add是将文件添加到暂存区
而使用git commit是往master分支上提交修改
 
如果暂存区没有内容，使用**git status**查看就发现
>nothing to commit, working tree clean
说明此时暂存区是干净的，没有东西需要提交


