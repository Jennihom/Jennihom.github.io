---
layout: post
title: "冗余样式清理机制"
description: ""
category: 
tags: []
---
{% include JB/setup %}

*1、现状*


项目初始时，样式文件没有分开，导致css文件巨大（122k）；

项目快速迭代、开发人员变更导致的css冗余；

*2、分析处理冗余样式的方法*


2.1、 浏览器工具

（1）Chrome Audits
	
仅仅告诉我们哪些样式没有用到，要想删除就需要比对原文件...

（2）firebug —— css usage

2.2、 [unused-css](http://unused-css.com "unused-css")

可视化工具，简单易用，but没啥用。。。

2.3、 [uncss](https://github.com/giakki/uncss "uncss")

（1）安装

	npm install -g uncss

（2）node运行

2.4、 [grunt-uncss](https://github.com/addyosmani/grunt-uncss "grunt-uncss")

（1）安装

	npm install grunt-uncss

（2）grunt 任务

*3、定制方案*


借助grunt、phantomjs、grunt-uncss实现自定义删除无用样式及按模块拆分样式。

（1）借助phantomjs批量生成静态html页面；
（2）再利用grunt-uncss删除冗余样式



*友情提示*


有了爆棚的信心、十足的把握后再开始吧~

