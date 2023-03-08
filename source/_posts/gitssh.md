---
title: gitssh
date: 2023-03-07 18:23:41
tags:
---
# 配置用户名
git config --global user.name "用户名"
# 配置邮箱
git config --global user.email "邮箱地址"
# git生成公钥
ssh-keygen -t rsa -C '邮箱地址'
# 查看git的用户名和邮箱
git config --global --list
# 查看git的公钥
$ cat ~/.ssh/id_rsa.pub
--------------------------------------------------------------------------
##git 常用命令记
提交 git commit
分支 git branch bugFix,git checkout bugFix   /git checkout -b bugFix


