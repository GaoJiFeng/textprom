# Git面试题

## 1、什么是Git

*Git 是一个开源的分布式版本控制系统，用于敏捷高效地处理任何或小或大的项目。*

*Git 是 Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。*

*Git 与常用的版本控制工具 CVS, Subversion 等不同，它采用了分布式版本库的方式，不必服务器端软件支持。*

## 2、Git常用的指令

### git add [file1-name] [file2-name] ...

\- 将文件暂存。

[file1-name]　　-　　文件名称

EX : git add file1 file2

### git commit -m 'add comment here'

\- 将所有已暂存起来的文件一并提交

### git commit -a -m 'add comment here'

\- 自动把所有已跟踪的文件暂存起来一并提交 （优点：可以省略 git add filename 这一步骤）

### **git commit --amend**

\- 修改上次commit的注释或内容

\- 如果仅修改上次commit的注释，则直接敲该命令即可

\- 如果需要修改或者增添文件等操作，需要先在本地对那些需要修改的文件进行修改，然后用giit add将这些修改加到暂存区中，之后再敲该命令，填写新的注释，提交，便可达到目的

## 3、Git的作用

主要用于多人协同开发一个项目

git是一种开源的分布式的vcs(version control system)版本控制系统。

优点是分布式的版本管理，对比集中式的版本管理系统来说不会出现中心服务器死机就影响工作，而是可以先存储在本地，等服务器修改好还可以接着进行工作，并且git的社区灵活，拥有丰富的资料来进行学习查阅，并且git是开源的，它强调个体，并且对于公共服务器压力不会太大，大小项目均可管理，拥有良好的分支机制，git的分支只要不提交合并，对其他人没有任何影响，并且git是统一管理元数据，存放在称为.git的文件目录里面。

git的版本之间的兼容性不好，可能在上个版本的项目内容放到另一个git版本会出错。


