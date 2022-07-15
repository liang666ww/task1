1.git init命令
在git bash中输入了该命令是创建了一个.git文件，但是这个文件是隐藏的，需要你把它设置成不隐藏
一般是在查看中设置，但是有的时候调成共享就行了
2.ll命令
查看该目录下有多少文件
3.touch +文件名
在该目录下创建一个文件
4.前言：
git status 输成git staus
git add . 输成git add.
git commit 输成git comit
都会报以下错误：
git: 'XXX' is not a git command. See 'git --help'.

The most similar command is
        add
这就要提醒你自己要输入正确了
5.git add .
是一次性把该文件下的所有子文件都上传到暂存区
6.git status
是检查此时此刻文件的位置状态
7.git commit报错：
（1）
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'lenovo@LAPTOP-LF6I5PNE.(none)')
说明该用户还没有注册（即没有身份）
解决办法：输入你的姓名你的邮箱完成注册即可
git config --global user.name "tom-gitee"
git config --global user.email "3023120094@qq.com"
（2）Aborting commit due to empty commit message.
说明你需要添加你的这次的改动情况： git commit -m "add file01"
8.因为你在git bash here 的时候又重新创建了git笔记这个文档所以你需要再次的git add和git commit -m""重新提交你的文件才能正常的git status
9.你的git的用户名叫 tom-gitee 或者liangwww
10.能够查到commitid的git命令 git reflog
回退到某一个版本是git reset --hard commitid
11.分支：
git branch 查看分支
git branch 分支名 就是添加了一个叫分支名的分支
分支的切换：git cheackout 分支名
HEAD所指向的分支名就是当前所在分支，你只能在一个分支下对仓库进行管理
所以你在dev01分支中添加了一个文件text02并且经过git add .和git commit -m" "的仓库管理工作后，你最后git log不同分支
看到的文件都是不同的（中间有一个分支切换git checkout 分支名 操作）
12.直接创建并切换到该分支 git checkout -b 分支名
13.合并分支：不同分支会开展不同的工作通常我们把其他分支的工作都合并到master分支上
先切换到master分支上,再git merge 分支名就能在master分支上合并该分支
