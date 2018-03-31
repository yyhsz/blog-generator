---
title: 如何用css制作一个太极图案
date: 2018-03-24 14:44:05
tags: [前端,CSS]
---
css功能多种多样，使用::before 和  ::after生成的伪元素可以在一个div元素中创造内部图案


## 先制作一个圆形
在html中定义一个div元素:
    
    <div class="yin-yang"></div>

在css中配置样式:

    .yin-yang {
            width: 100px;
	        height: 50px;
	        background: white;
            border:1px solid black;
            border-width:1px 1px 51px 1px;/*用来填充圆形下半部分，51px=50px元素背景+1px边框使上下对称*/
            border-radius:50%;  /*定义边框半径占整体的比例，越接近50%越像一个圆*/
            position:relative;/*与下面的伪元素position配合使用*/
    }
	
<!-- more -->

## 制作圆内伪元素
在css中配置样式：

      .yin-yang::before {
	         content: "";
             position:absolute;/*不为元素预留空间，通过指定元素相对于最近的非 static 定位祖先元素(即yin-yang)的偏移，来确定元素位置*/
             height:15px;
             width:15px;/*定义元素（即太极图案内部小洞洞）大小*/
             background: white;
             border-radius:50%;
             border:17.5px black solid;/*太极内部圆的大小*/
            margin-top:20px;/*也可以用 top来定位*/   }

    .yin-yang::after {
	         content: "";
             position:absolute;
             height:15px;
             width:15px;
             background:black;   
             border-radius:50%; 
             border:17.5px white solid;
             margin-left:50px;
             margin-top:20px /*也可以用top和left来定位*/   }
<br>

最终结果：![捕获.PNG](https://upload-images.jianshu.io/upload_images/11120567-fc5935be70bf2525.PNG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240) 


参考来自  css.tricks(好像要科学上网才能看):  https://css-tricks.com/examples/ShapesOfCSS/

