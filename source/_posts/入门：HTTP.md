---
title: 入门：HTTP 笔记
date: 2018-03-31 19:36:45
tags: 前端
---

<h2>http入门</h2>

<h4>一些零碎的知识点</h4>
- www:world wide web,万维网之父：Tim Berners-Lee

- URI(统一资源标识符):uniform resource identifier

- URL(统一资源定位符):uniform resource locator

- URN(统一资源命名符)：uniform resource name

通过urn来确定一个<em>唯一</em> 的资源
通过url来确定一个地址（网址）但不清楚其中内容是什么，并且其内容可以更换
uri是url和urn的统称,URN定义某事物的身份，而URL提供查找该事物的方法。

![url](https://i.loli.net/2018/03/31/5abf6f72acaa0.jpg)
<!--more-->

- DNS(域名系统):domain name system
是互联网的一项服务。它作为将域名和IP地址相互映射的一个分布式数据库

- 修改host文件可以暂时科学上网
- .com , .cn , .mobi etc 是顶级（一级）域名 ； xxx是二级域名 ；www.   是三级域名 ； （交流中默认xxx是一级域名）

<h2>请求与响应</h2>

![请求与响应](https://i.loli.net/2018/03/31/5abf72dfc38cb.jpg)
http协议下服务器与浏览器一般是单项访问，如同打乒乓
使用qq聊天就不能算是http协议
每一台服务器有很多端口，每一个端口只有一种功能,其中80端口是用于服务http协议,如果要做一个后台服务器，必须将80端口暴露给人用
- 浏览器负责发起请求
- 服务器在80端口接收请求
- 服务器负责返回内容（响应）
- 浏览器负责下载响应内容
HTTP的作用就是指导浏览器和服务器的沟通
<hr>
    
    curl -s -v -H "lalala" -- "www.baidu.com"
curl:发出网络请求并接收数据s:不要显示进度 v:使请求和响应更详细 -H：显示请求头

发出请求：

    1. 动词(GET/POST) 路径(/xxx) 协议/版本(HTTP/1.1)
    2. Key1: value1
    2. Key2: value2
    2. Key3: value3
    2. 希望返回内容:xxx/xxx(Accept:text/html)
    2. 用户代理：xxxx(User-Agent:curl/xxxx)
    2. 访问主机：(Host:xxxx)
    3. (回车)
    4. 要上传的数据

响应：

    1. 协议/版本号 状态码 状态解释
    2 Key1: value1
    2 Key2: value2
    2 Content-Length: 17931
    2 Content-Type: text/html;charset:utf-8;
    3
    4 要下载的内容

可以用开发者工具的Network查看响应的第4部分