### 目录
> * [环境配置](https://py3.io/doc/python/quickstart.html)
> * 基础命令
> * vi文本编辑器
> * Shell与Shell脚本
> * 软件管理
> * 网络基础
>   * XXX
>   * requests使用多IP请求
>   * [Python多线程模板](code/MultiThread_Template.py)

&nbsp; 

&nbsp; 

### 🥉学习方法

* 你现在已经有了一些Linux的基础了，应该系统学一下了
* 先把韦东山嵌入式Linux完整看一遍(不要全看，挑着看  
* 看经典书籍（鸟哥的Linux私房菜很不错）
* 看大佬们的有关源码   
* 找2-3个相关项目巩固一下，最好能写在简历上 
* 刷题   

### ❓未解决的问题
1、Windows下ipconfig出问题了  
2、Mobaxterm不能远程登录Ubuntu    

3、FileZilla连接不上Ubuntu

解决方法：

#### 1、打开本机服务，开启相关的服务。

![image-20230922230558170](C:\Users\东瑞\Desktop\222\Notes\images\image-20230922230558170.png)

#### &nbsp; 2、重置虚拟网络编辑器

&nbsp;&nbsp;打开虚拟网络编辑器—>还原默认设置

![image-20230922230646609](C:\Users\东瑞\Desktop\222\Notes\images\image-20230922230646609.png)

&nbsp;&nbsp;还原默认设置之后，就看见有了虚拟机的网卡了

![image-20230922230837506](C:\Users\东瑞\Desktop\222\Notes\images\image-20230922230837506.png)


#### 第一节
* 绝对路径用 \   相对路径用 /

* Shell命令  PATH环境变量设置

* ./ 表示当前目录下行命令  

* 在Linux系统中，每个设备都被当成一个文件来对待，例如SATA接口的硬盘文件名为 /dev/sd[a-d]  

* 绝对路径进入 cd /home/alien  

* 相对路径进入 cd ./XXX/  

  &nbsp; 


### 📉基础命令

| 命令    | 意义             | 用法                       | 说明                                                         |
| ------- | ---------------- | -------------------------- | :----------------------------------------------------------- |
| pwd     |                  |                            | 显示当前目录                                                 |
| cd      |                  | cd ..                      | 上一级目录                                                   |
|         |                  | cd ~                       | 进入家目录                                                   |
|         |                  | cd -                       | 切回上一次操作的目录                                         |
| cp      |                  | cp a b                     | 将a复制一份命名为b                                           |
| ls      |                  | ls -l                      | 查看文件的属性权限                                           |
| mkdir   |                  |                            | 创建目录                                                     |
| rmdir   |                  |                            | 删除目录 （只能删除空目录）                                  |
| rm      |                  | rm -rf <目录路径>          |                                                              |
| echo    |                  | echo abc > 1.1.txt         | 创建一个文件                                                 |
| cat     |                  |                            | 列出文件的内容                                               |
| touch a |                  | touch a                    | 摸一下该文件，只改时间，不改内容                             |
| mv      |                  | mv a ../                   | 将a移动到上一级目录里                                        |
|         |                  | mv ../a .                  | 将上一级目录里的a移动到当前目录                              |
| tab键   |                  |                            | tab键  补全当前目录下的文件名                                |
| chmod   |                  | chmod 675 <某个文件>       | 改变文件的权限（拥有者、同组其他用户和其他用户的可读r、可写w、可执行r等） |
|         |                  | chmod -x <某个文件>        | 权限全部去掉                                                 |
| chowm   | 改变文件的所有者 | chown root root <某个文件> | 改变文件的拥有者、其他用户等                                 |
| root    |                  |                            | 用户切换、登录、设置密码（不建议用                           |
| sudo    |                  |                            | 临时切换为root用户  这个命令nb                               |
| find    |                  | find abc -name *.1.txt     | 指定当前目录下的abc文件夹下查找名字为1.1.txt、2.1.txt等文件  |
| grep    |                  | grep "xyz" * -nwr          | 递归查找当前目录下的所以文件中含有xyz字符的文件              |
| tar     | 压缩             | tar czf abc def            | 创建压缩包 用gzip命令压缩 将def文件压缩为名为abc的压缩包（也可以压缩目录） |
|         | 解压             | tar xzf abc -C aaa         | 将压缩包abc解压到aaa目录里去 用gzip解压                      |
| man     |                  |                            |                                                              |

### &nbsp; 

### 📉vi命令

![image](https://github.com/zhaodaer/Notes/assets/141413040/0ef785b2-29ad-425a-b9b7-d1534f6e392d)
&emsp;保存退出        :wq  
&emsp;不保存退出       :q!  
&emsp;:set number   显示行号  
&emsp;:set nonumber   不显示行号  
&emsp;:256  跳到第256行  
&emsp;ctrl+f  向前翻页  
&emsp;ctrl+b  向后翻页  
&emsp;G:跳到文件结尾  
&emsp;0:跳到行首  
&emsp;$:跳到行尾  

#### 编辑  
&emsp;插入:输入i进入编辑模式  
&emsp;删除:  
&emsp;x:删除-一个字母  
&emsp;dw: del word  
&emsp;D:删除光标之后的内容  
&emsp;dd:删除整行  
&emsp;ndd //删除当前行及其后的n-1行(n是数字)  
&emsp;o:在当前行下面新增加--行  
&emsp;u:撤销上一-步操作  

#### 复制/粘贴  
&emsp;yy:复制当前行(y:yank(复制))   
&emsp;nyy:复制当前行及其后的n-1 行(n是数字)  
&emsp;p:粘贴(p :paste)  

#### 查找/替换  
&emsp;/pattern: 从光标开始处向文件尾搜索pattern, 后按下n(向下查找)或N(向上查找)  
&emsp;:8s/p1/p2/g :将文件中所有的p1均用p2替换  
&emsp;:8s/p1/p2/gc :替换时需要确认  


#### 测试NAT网卡能不能用：
&emsp;利用ping www.baidu.com 测试
&emsp;不行的话 打开服务，把关于VMware的所有服务都启动

#### 用Source insight 来阅读源码(要破解，有点麻烦，我选择VScode)

#### Mount命令录制宏

&nbsp; 

&nbsp; 

&nbsp; 

### 📉gcc编译器

#### 编译过程：

![image-20230922115433188](C:\Users\东瑞\Desktop\222\Notes\images\image-20230922115433188.png)

#### 编译多个文件

一起编译、链接：

```c
gcc -o test a.c b.c
```

分开编译，统一链接：

```c
gcc -c -o a.o a.c
gcc -c -o b.o b.c
gcc -o test a.o b.o
```



#### 制作和使用动态库、静态库

#### 一些很有用的选项

![image-20230922122713220](C:\Users\东瑞\Desktop\222\Notes\images\image-20230922122713220.png)

&emsp;gcc -E main.c // 查看预处理结果，比如头文件是哪个
&emsp;gcc -E -dM main.c > 1.txt // 把所有的宏展开，存在 1.txt 里
&emsp;gcc -Wp,-MD,abc.dep -c -o main.o main.c // 生成依赖文件 abc.dep ，后面 Makefile 会用
&emsp;echo 'main(){}'| gcc -E -v - // 它会列出头文件目录、库目录(LIBRARY_PATH)

&nbsp; 

&nbsp; 

&nbsp; 

### 📉Shell脚本







### 📉Makefile

1、最简单的：

```c
gcc -o test a.c b.c
```

查看编译的详细信息：

```c
gcc -o test a.c b.c -v
```

<font color=red>缺点</font>：修改一个文件再编译，会对所有的文件重新编译

2、Makefile核心---规则：

&emsp;&emsp;目标文件：依赖文件1  依赖文件2
&emsp;&emsp;`[TAB]` 命令

&emsp;&emsp;当"目标文件"不存在，或某个依赖文件比目标文件"新" ，则:
&emsp;&emsp;执行"命令"规则：

```c
test : a.o b.o
	gcc -o test a.o b.o
a.o : a.c
	gcc -c -o a.o a.c
b.o : b.c
	gcc -c -o b.o b.c
```



#### 语法：

**1、通配符**（若有很多文件，则使用）：

$@：表示目标

$<：表示第1个依赖文件

$^：表示所有依赖文件

```c
test : a.o b.o c.o
	gcc -o test $^
%.o : %.c
	gcc -c -o $@ $<
```



**2、假想目标（.PHONY）**：

```c
test : a.o b.o c.o
	gcc -o test $^
%.o : %.c
	gcc -c -o $@ $<

clean :
	rm *.o test
.PHONY : clean
```



**3、即时变量、延时变量**：

:=     即使变量，即刻确定，在定义时就确定了

=      延时变量，使用时才确定它的值

?=     延时变量，只有1次定义值才起效

+=     附加，是即时变量还是延时变量取决于前面的定义

```c
a := $(c)
b = $(c)
c = abc
d = 100
d ?= 2000

all :
   @echo a = $(a)
   @echo b = $(b)
   @echo c = $(d)

c += 123
```


**结果**：a = 无

&emsp;&emsp;&emsp;b = abc 123

&emsp;&emsp;&emsp;c= 100 



**4、Makefile函数**：

**程序：**

```c
A = a b c
B = $ (foreach f, $(A)，$(f).o)	//将A中的所有文件加上.o

C = a b c d/
D = $ (filter  %/, $(C) )	//找出在C中所有符合%/的文件
E = $ (filter-out  %/, $ (C) )	//找出在C中所有不符合%/的文件

files = a.c b.c c.c d.c e.c abc
files2 = $ (wildcard  $ (files) )	//取出files中处在的文件
dep_files = $ (patsubst %.c, %.d, $(files) )
    		//从files2中取出所有文件，找出符合.c的文件，然后全部替换成.d文件
    
all :
	@echo B = $ (B)
	@echo D = $ (D)
	@echo E = $ (E)
	@echo files2 = $ (files2)
    @dep_files = $ (dep_files)
```

**输出：**

```c
B = a.o b.o c.o
D = d/
E = a b c
files2 = a.c b.c c.c
dep_files = a.d b.d c.d d.d e.d abc
```



**命令格式**：`make [目标]`

&emsp;单独使用make命令，只执行第一个test命令，不会执行其他的。但使用make clean时只执行clean命令



**通用Makefile的使用**：

[链接](E:\learn\weidongshan_Linux\01_all_series_quickstart\04_嵌入式Linux应用开发基础知识\doc_pic\01.嵌入式Linux应用开发基础知识.docx)

![image-20230924210303604](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230924210303604.png)





### 📉文件IO



#### 怎么访问文件?

**通用的IO模型**：open/read/write/lseek/close
**不是通用的函数**： ioctl/mmapl

把SD卡插到开发板上，挂载它的分区，然后去访问对应的目录就可以了



主设备号表示哪一个驱动，次设备号表示这个设备里面的哪一个硬件





### 📉多线程编程

### 📉网络编程

### 📉I2C应用编程

### 📉驱动内核



