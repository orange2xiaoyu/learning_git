Git is a version control system.

Git is free software.

Create a new branch is quick and simple.

hello world!

## git的基本使用
安装完git之后，如果想要使用git管理仓库，需要先设置自己的名字与邮箱：

git config --global user.name "xiaoyu"

git config --global user.email "xiaoyu@example.com"


### 创建版本库
首先创建一个空目录，然后将其初始化，使其变为可以使用git管理的仓库：

mkdir learngit

cd learngit

git init

使用ctrl+h可以看到文件夹中隐藏的文件。

### 将文件添加到版本库
使用git add，将文件添加到仓库

git add <file>

eg: git add readme.txt

使用git commit，将文件提交到仓库

git commit -m <message>

eg: git commit -m "add readme.txt"

git commit 命令中，-m后面加的是比较的说明。git add可以重复使用，添加多个文件到仓库，然后使用git commit可以一次性全部提交。

### 查看仓库状态
使用git status 查看当前仓库的状态

git status

输出为：

On branch master

nothing to commit, working directory clean

将readme.txt进行修改，可以使用git status查看当前状态

输出为:

On branch master

Changes not staged for commit:

  (use "git add <file>..." to update what will be committed)

  (use "git checkout -- <file>..." to discard changes in working directory)

         modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")

git status

并且我们可以使用git diff查看修改前后的不同：

git diff readme.txt


输出为：

diff --git a/readme.txt b/readme.txt

index f1dc24f..1bc5139 100644

--- a/readme.txt

+++ b/readme.txt

@@ -1,2 +1,4 @@

Git is a version control system.

-GIt is free software.

+Git is free software.

+

### 查看提交日志
使用git log可以查看从最近到最远的提交日志：

git log 

输出

commit 533ff2b718ee32fcc20c23cf09d59ea51c50fde4  # 表示commit id(版本号)
Author: xiaoyu <xiaoyu@example.com>
Date:   Tue Aug 27 10:42:10 2019 +0800

### 查看提交日志

使用git log可以查看从最近到最远的提交日志：

git log 
