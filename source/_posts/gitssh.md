---
title: git and ssh
date: 2023-03-07 18:23:41
tags: [git,ssh,svn]
---
# 配置用户名
``` bash
git config --global user.name "用户名" 
```
# 配置邮箱
``` bash
 git config --global user.email` "邮箱地址"
 ```
# git生成公钥  
>   会生成在当前目录，git bash到用户的.ssh文件夹，可命名文件名，可设置打开文件的密码.默认电脑一个公钥私钥，一个公钥只能被使用一次，建议公钥绑定github账号而非github具体的仓库，部署多个[点击这里](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/managing-deploy-keys)
``` bash 
 ssh-keygen -t rsa -C '邮箱地址'
``` 
<!-- more -->
# 查看git的用户名和邮箱
``` bash
 git config --global --list
 ```
# 查看git的公钥
存储就在用户目录下的.ssh文件夹里
``` bash
cat ~/.ssh/id_rsa.pub
```
--------------------------------------------------------------------------
# 创建git仓库
1.先在账户上创建repository。保证用户有权限，SSH或者http登录，推荐SSH绑定账户信息，http登录仓库，方便权限管理

2.a 没有.git文件的，先在本地工程一级目录下初始化
``` bash
echo "# HexoBogForPanpan" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:pansansui/HexoBogForPanpan.git //这是在你电脑上生成了一个origin的远程仓库，连接地址是后面的，常用命令有git remote //列出远程仓库名
git remote show [远程仓库名] //该仓库链接的详细信息
git remote rename old-name new-name //换名
git push -u origin main //发布到远程仓库
```
2.b 有.git文件的:
``` bash
git remote add origin git@github.com:pansansui/HexoBogForPanpan.git
git branch -M main
git push -u origin main
```

# git 常用命令集
git 常用操作练习[点击这里](https://learngitbranching.js.org/?locale=zh_CN)，该网站常用命令show solution，reset，levels
删除当前项目的git关联
`find . -name ".git" | xargs rm -rf`
初始化 
`git init`
查看追踪文件状态 
`git status`
取消文件追踪  
`git reset HEAD [文件路径]`
添加文件追踪 
`git add [文件]`
提交
 `git commit -m [本次更新的消息提示]`
创建切换分支 
`git branch bugFix;git checkout bugFix`
或者
`git checkout -b bugFix`
合并当前分支与目标
`git merge [目标分支]`
<img src=/images/merge.png width="30%" alt="未找到merge流程图片" >
`git rebase [目标分支]`

