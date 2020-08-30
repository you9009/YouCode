---
title: [关于Git命令]
description: [一些关于git常用的日常命令]]
---

# Git命令

## 创建新项目
```bash
git init
git add .
git commit -m "init"
git remote add origin 库名
git push -u origin master
```


## 安装及配置

- 配置用户名：git config --global [user.name](http://user.name) "你的名字"
- 配置e-mail：git config --global user.email "你的邮箱@xx.com"



## 分支管理

- 创建分支：git branch 库名
- 切换分支：git checkout 库名
- 删除分支：git branch -d 库名
- 合并分支：git merge 库名
- 合并分支把树杈掰到主干上：git rebase
- 连接远程仓库：git remote add origin 库名
- 查看远程仓库：git remote -v
- 删除远程仓库：git remote rm 库名
- 拉取远程仓库：git pull origin 库名

## 与添加有关的

- 将当前目录变为仓库：git init
- 将文件添加到暂存区：git add .
- 将文件添加到暂存区：git add -A
- 将暂存区提交到仓库：git commit –m "描述"
- 提交暂存：git push / git push -u origin 库名

## 与查询有关的

- 查询仓库状态：git status
- 比较文件差异（请在git add之前使用）：git diff 文件名
- 查看仓库历史记录(详细)：git log
- 查看仓库历史记录(单行)：git log --pretty=online 或 git log --online
- 查看所有版本的commit ID：git reflog



## 与撤销有关的

- 撤销工作区的修改：git checkout -- 文件名
- 撤销暂存区的修改：git reset HEAD 文件名
- 回退到指定历史版本：git reset --hard 该版本ID
- 回退到上个版本：git reset --hard HEAD^
- 上上版本是HEAD^^，也可用HEAD~2表示，以此类推



## 与标签有关的

- 为当前版本打标签：git tag 标签名
- 为历史版本打标签：git tag 标签名 该版本ID
- 指定标签说明：git tag –a 标签名 –m "标签说明" [可选：版本ID]
- 查看所有标签：git tag
- 查看某一标签：git show 标签名
- 删除本地某一标签：git tag –d 标签名
- 删除远程t标签：git push origin :refs/tags/标签名
