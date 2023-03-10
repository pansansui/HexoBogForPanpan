---
title: hexoOceanSkill
date: 2023-03-08 18:33:59
tags: ["blog","hexo"]
---
ocean 主题的feathericon的代号映射位置在themes\ocean\source\css\_feathericon.styl下
ocean 主题的菜单更改图标的文件在themes\ocean\source\css\_partial\navbar.styl中
# 遇到的问题:
制作谷歌播放器动画的时候，声明在themes\ocean\source\css\_partial\layout.styl 的属性绑定不了上iframe，最后在themes\ocean\source\js\ocean.js中用jQuery绑定的，原因初步~~推测是要等iframe渲染好才可以绑定style属性。~~
---发现部署在github上的和自己hexo server运行的不一样，且导航栏的颜色属性也莫名奇妙的被覆盖了，现在怀疑是hexo g的时候哪里覆盖了layout.styl的属性或者根本没用上。
---真搞不懂了，在layout.styl删除了@media (min-width: 768px)下面的sidebar所有属性后，github上的导航栏恢复正常了，注释掉ocean.js的播放器动画，声明在layout.styl上也行了，问题是sidebar的颜色前后声明都是一样的为啥后面不行。
--受不了啦，明明写的right为-10rem喵的hexo g编译老是给爷改成10rem，最后2023手动改了public里的ocean.js和styl.styl，to do ：实现手机端的播放器透明，不透明转换，顶端粘粘。