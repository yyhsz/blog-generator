---
title: 用Hexo+Github搭建一个博客
date: 2018-03-07 20:48:05
tags: Github  Hexo
---

#安装Hexo
    npm install -g hexo-cli

#Github上创建一个新仓库
    在 GitHub 上新建一个空 repo，repo 名称是「你的用户名.github.io」（请将你的用户名替换成真正的用户名）

#创建目录
    创建一个文件夹，用Gitbash打开该文件夹，并执行以下指令，Hexo 即会自动在目标文件夹建立网站所需要的所有文件
    hexo init

#安装依赖包
    npm install

#编辑网站配置
   用vs code编辑 _config.yml 文件
    1.把第 6 行的 title 改成你想要的名字
    2.把第 9 行的 author 改成你的大名
    3.把最后一行的 type 改成 type: git
    4.在最后一行后面新增一行，左边与 type 平齐，加上一行 repo: 仓库地址 （请将仓库地址改为「你的用户名.github.io」对应的仓库地址

#安装 git 部署插件
    npm install hexo-deployer-git --save

#生成网页并部署
    hexo generate
    hexo deploy
    以下提示说明部署成功：[info] Deploy done: git



