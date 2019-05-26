# 基础概念

1. 每一份 Git 版本库均包含着此版本库所有文件的所有修改及提交历史，远程和本地的区别只是存在的位置不同
2. 工作区，即当前文件夹
3. 版本库，包含了受监控的所有文件的所有修改记录，其中包括了暂存区及版本库分支，默认分支为 master，通过 git add 命令将文件提交到暂存区，通过 git commit 命令将文件提交到分支

## 新建版本库

1. git config --global user.name "xxx"
2. git config --global user.email "xxx"
3. git init —— 初始化版本库，此时什么事情都还未发生，仅仅是建立了空的版本库
4. git add <file> —— 添加文件到暂存区，告诉 Git 对哪些文件进行监控
5. git commit -m "xxx" —— 提交到版本库，将改变提交到版本库成为最新的文件版本，参数 m 后为提交说明

## Clone 版本库

## 查看版本库状态

1. git status 或可视化管理器 —— 此命令会详细列出所有文件的修改情况
2. git diff <file> —— 此命令会详细列出此文件的修改情况，按 q 退出

## 提交修改

1. git add <file> —— 添加文件到暂存区，告诉 Git 对哪些文件进行监控
2. git commit -am "xxx" —— 提交到版本库，将改变提交到版本库成为最新的文件版本，参数 m 后为提交说明

## 同步到远程库

1. git remote add origin "xxx.git" —— 设置远程版本库
2. git push -u origin master —— 在本地提交后将当前分支提交到远程版本库，u 参数仅在第一次推送时候使用，作用是将本地的 master 分支与远程的 master 分支关联起来
3. git remote rm origin —— 取消当前设置的远程版本库

## 安装 Visual Studio Code 扩展

1. Git Project Manager —— 可视化进行源代码管理
2. GitLens —— 跟踪版本库，提示每一行代码版本历史
3. Git History —— 可视化浏览版本历史记录

## 常用命令

1. 找回文件版本
2. git checkout —— 将文件从版本库中恢复到工作区
3. git rm —— 删除文件

先创建远程库，再 clone 到本地
git clone "xxx.git"

创建用于 ssh 连接的秘钥
ssh-keygen -t rsa -C "x@x.x" —— 创建 ssh 秘钥，其中id_rsa为私钥，id_rsa.pub为公钥