---
title: html_CSS
date: 2023-03-13 17:22:53
tags: ["html",["css"]]
---
div内文字： 
a. 字母时，空格区别一个单词，换行时不会切割单词。
b. 汉字时，自动换行。
<!-- more -->
把div当作模板时，可以遮住iframe，遮不住select。可以使用iframe可以遮盖select，一般使用iframe和div结合的办法遮盖select（div所以要比iframe的z索引高）并创建内容，其实iframe会自动隐藏select，也可以自己只使用div和js隐藏select。如本博客主页所遇到的,下面的div用来在移动端时，遮住音乐播放器，和主页select视频，放弃hover事件模拟播放器iframe的点击事件。
```bash
<div class="musicMobileCover">
      <iframe hidden>
      </iframe>
</div>
```
