---
layout: post
title: 	前端乱麻梳理
date: 2018-11-19 13:24:00 +08
update: 2018-11-9 13:24:00 +08
categories: front-end
---

# 用Vue和它配套的各种开箱即用的工具，但却没有去自习研究这些工具到底是如何工作，这边文章用于记录总结。

## javascript && nodejs
javascript 语法一样，但运行于不同的环境中，提供不同的api。
常见的浏览器和Nodejs环境。 浏览器环境提供dom api等，更多的与浏览器交互； Nodejs 环境提供操作系统，文件系统，网络等api，有更多的能力和操作系统交互。

## npm
nodejs 包管理工具，管理nodejs中依赖。可以获取全世界别人的轮子，也可以自己写贡献给他人。
值得一提的是包可以拥有单独可执行程序，所以很多有用的工具都可以通过npm发布，比如webpack。

## webpack
模块打包成勋。nodejs中可以使用 import require 等引入模块，但浏览器中无法运行， webpack程序将代码使用的模块重新打包组织，从而可以在浏览器中运行。
最基本的功能打包js包; 同时通过loader可以转换指定类型的非js模块为js模块，类如css,vue,image等; 更进一步plugin可以进一步处理代码运行程序等。
