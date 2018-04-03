---
title: 用Hexo+Github搭建一个博客（不完全指南）
date: 2018-03-07 20:48:05
tags: [前端,] 
---

<h4> 安装Hexo</h4>
 在gitbash 中输入：
 
    npm install -g hexo-cli

<h4>Github上创建一个新仓库</h4>
在 GitHub 上新建一个空 repo，repo 名称是「你的用户名.github.io」（请将你的用户名替换成真正的用户名）

<h4>创建目录</h4>
在任意空白处创建一个文件夹，用Gitbash打开该文件夹，并执行以下指令

    hexo init
Hexo 即会自动在目标文件夹建立网站所需要的所有文件
    

	
<!-- more -->

<h4>安装依赖包</h4>

    npm install

<h4>编辑网站配置</h4>
   用vs code编辑 _config.yml 文件
    1.把第 6 行的 title 改成你想要的名字
    2.把第 9 行的 author 改成你的大名
    3.把最后一行的 type 改成 type: git
    4.在最后一行后面新增一行，左边与 type 平齐，加上一行 repo: 仓库地址 （请将仓库地址改为「你的用户名.github.io」对应的仓库地址

<h4>安装 git 部署插件</h4>

    npm install hexo-deployer-git --save
	


<h4>生成网页并部署</h4>
gitbash中输入

    hexo generate
    hexo deploy
出现以下提示说明部署成功：

    [info] Deploy done: git



