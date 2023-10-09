---
title: Markdown使用说明
date: 2023-08-07 22:29:09
categories: 
- Markdown
copyright: false
cover: 
swiper_index: 1 yi、要在Markdown编辑器中实现按下tab效果，只需在文档中写入：
---



<!--more-->

## 一、空格、换行

tab效果：这里有—>&emsp;
![在这里插入图片描述](https://img-blog.csdnimg.cn/178e1ebfaf974a3f962cbf9ed310a7d5.png)

&nbsp; 

空格效果：这里有—> &nbsp;
![在这里插入图片描述](https://img-blog.csdnimg.cn/f4b020b979374ed0bf584a62ccc08b54.png)

&nbsp; 

换行：tab或空格后加一个空格

这里有—>&emsp; 

&emsp;  

&emsp;  

![在这里插入图片描述](https://img-blog.csdnimg.cn/bd956dc8223a4edb8ce6e744253c3705.png)

以下是渲染效果：

>   这句话前面有个tab，且它下面有两个空行
>  
>  
>  这句话前面有个空格，且它上面有两个空行





## 二、更改字体大小、颜色、更改字体

<font face="逐浪新宋">我是逐浪新宋</font>
<font face="逐浪圆体">我是逐浪圆体</font>
<font face="逐浪花体">我是逐浪花体</font>
<font face="逐浪像素字">我是逐浪像素字</font>
<font face="华文楷体">我是华文楷体</font>

&emsp;  

<font color=red>我是红色</font>
<font color=#008000>我是绿色</font>
<font color=yellow>我是黄色</font>
<font color=Blue>我是蓝色</font>
<font color= #871F78>我是紫色</font>
<font color= #DCDCDC>我是浅灰色</font>

&emsp;  <font size=5>我是尺寸</font>
<font size=10>我是尺寸</font>
<font face="逐浪立楷" color=green size=10>我是逐浪立楷，绿色，尺寸为5</font>



## 三、居中居右居左

> 居中`<center>文本</center>`
> 居右`<p align="right">文本</p>`
> 居左`<p align="left">文本</p>`

&emsp; 

## 四、加粗

**我是加粗**

&emsp; 

&emsp; 

## 五、插入图片

&emsp;&emsp;采用相对路径，**注意**图片地址和.md在同一文件夹下：

```text
![Alternative text](link "optional title")
```

![这是图片](20230821204027.jpg "Magic Gardens")

**注释：**

> Alternative text：替代文本，即当图片不能正常显示的时候显示的文本。这个字段中不能有空格，如果一定要填空格可以使用`%20`代替，我一般是使用下划线代替空格~
>
> Link：图片的本地地址，或者网络地址，这个地址最好选择相对地址，不能使用绝对地址，如果非要引用不同文件夹的文件，那么解决办法在下面~
>
> Optional Title：鼠标悬停的时候显示的标题和文字，可以不写
