---
title: pansansuiBlog
date: 2023-03-09 15:24:40
tags: [blog,hexo,ocean]
---
# 本博客的框架和解构（Hexo框架，Ocean主题）
完全自己一个人摸索的，理解不一定正确
## 工程结构
> node_modules----------------------------npm下载的各种依赖插件，hexo服务器，各类hexo的插件
> public----------------------------------hexo给你的工程编译后的工程结构，实际上你开发的项目部署时的结构
> scaffolds----------------------------模板，hexo new 可以按照里面的模板来生产Markdown
>> draft ----------------------------blog的草稿文件模板he
>> post----------------------------发布的blog模板
>> page----------------------------页面模板!!!区分blog和页面，
>
> source----------------------------对应scaffolds模板创建出来的文件，写博文主要在这个文件下面编辑
>> _draft
>> _posts
>> about
>> gallery
>> link
>> video
>
> themes----------------------------主题
>>landscape-----------landscape据了解是设计hexo主题的一个框架没用ocean主题应该把landscape文件名改成ocean，再根据结构开发
>>ocean
>>>languages
>>>layout
>>>>layout.ejs---------------------------- 每个页面的入口文件
>>>_config.yml ----------------------------ocean主题的配置文件
>
> _config.landscape.yml
> _config.yml hexo的配置文件
