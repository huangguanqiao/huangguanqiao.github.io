---
layout:     post
title:      Jenkins Introduction
subtitle:   BY Guanqiao Huang
date:       2021-02-02
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - Jenkins
---
1. CI/CD工具
Travis
Jenkins 默认认为运行在linux， 去做Pipeline的工具 engine/runner
Azure DevOps
Github Actions

2. 运行环境
- Node.JS
Node, NPM

- java
Maven, JDK
=> Pulisher: Oracle, OpenJDK, Amazon
version 8

- C#
Windows? Linux?
.Net Framework, .NET Core
=> .NET 6.0

【重点】对于环境配置，不同版本， 要和谐并存

3. Jekins
Scheduling
Orchestrating
Runner
Trigger
manage

4. 关于编程语言
不需要build的语言：
No build: js, py, shell, html, sql
所有脚本类的不需要build
对于这种就是version control替换到生产环境上

需要build的：java， clang， golang， c#， c++， VB， Swift， Obj-C
build出来是binary file，是要编译的
Node.js -> npm build -> package + optimize 没有调用的直接删掉，主要是打包各种脚本。没有被转换成二进制

自动拉去仓库里的代码，自动化部署
[CI/CD介绍](https://github.com/JiangRenDevOps/DevOpsLectureNotesV6/tree/master/WK4_Jenkins/Wk4.1/1.Ubuntu-install)