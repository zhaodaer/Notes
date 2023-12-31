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

[TOC]



##### 🥉碎碎念

---

* 你现在已经有了一些Linux的基础了，应该系统学一下了

* 先把韦东山嵌入式Linux完整看一遍(不要全看，挑着看  

* 看经典书籍（鸟哥的Linux私房菜很不错）

* 看大佬们的有关源码   

* 找2-3个相关项目巩固一下，最好能写在简历上 

* 刷题   

  &emsp; 

### ❓遇到的问题

---

1、Windows下ipconfig出问题了  

2、Mobaxterm不能远程登录Ubuntu    

3、FileZilla连接不上Ubuntu

**解决方法**：

**打开本机服务，开启相关的服务**

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214018290.png" width="500"/>

&nbsp; **重置虚拟网络编辑器**

&nbsp;&nbsp;打开虚拟网络编辑器—>还原默认设置

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214034861.png" width="500"/>



&nbsp;&nbsp;**还原默认设置之后，就看见有了虚拟机的网卡了**

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214236693.png" width="500"/>

---

### START

* 绝对路径用 \   相对路径用 /

* Shell命令  PATH环境变量设置

* ./ 表示当前目录下行命令  

* 在Linux系统中，每个设备都被当成一个文件来对待，例如SATA接口的硬盘文件名为 /dev/sd[a-d]  

* 绝对路径进入 cd /home/alien  

* 相对路径进入 cd ./XXX/  

  

### 📉基础命令

---

| 命令    | 意义                                     | 用法                       | 说明                                                         |
| ------- | ---------------------------------------- | -------------------------- | :----------------------------------------------------------- |
| pwd     |                                          |                            | 显示当前目录                                                 |
| cd      |                                          | cd ..                      | 上一级目录                                                   |
|         |                                          | cd ~                       | 进入家目录                                                   |
|         |                                          | cd -                       | 切回上一次操作的目录                                         |
| cp      |                                          | cp a b                     | 将a复制一份命名为b                                           |
| ls      |                                          | ls -l                      | 查看文件的属性权限                                           |
| mkdir   |                                          |                            | 创建目录                                                     |
| rmdir   |                                          |                            | 删除目录 （只能删除空目录）                                  |
| rm      |                                          | rm -rf <目录路径>          |                                                              |
| echo    |                                          | echo abc > 1.1.txt         | 创建一个文件                                                 |
| cat     |                                          |                            | 列出文件的内容                                               |
| touch a |                                          | touch a                    | 摸一下该文件，只改时间，不改内容                             |
| mv      |                                          | mv a ../                   | 将a移动到上一级目录里                                        |
|         |                                          | mv ../a .                  | 将上一级目录里的a移动到当前目录                              |
| tab键   |                                          |                            | tab键  补全当前目录下的文件名                                |
| chmod   |                                          | chmod 675 <某个文件>       | 改变文件的权限（拥有者、同组其他用户和其他用户的可读r、可写w、可执行r等） |
|         |                                          | chmod -x <某个文件>        | 权限全部去掉                                                 |
| chowm   | 改变文件的所有者                         | chown root root <某个文件> | 改变文件的拥有者、其他用户等                                 |
| root    |                                          |                            | 用户切换、登录、设置密码（不建议用                           |
| sudo    |                                          |                            | 临时切换为root用户  这个命令nb                               |
| find    |                                          | find abc -name *.1.txt     | 指定当前目录下的abc文件夹下查找名字为1.1.txt、2.1.txt等文件  |
| grep    |                                          | grep "xyz" * -nwr          | 递归查找当前目录下的所以文件中含有xyz字符的文件              |
| tar     | 压缩                                     | tar czf abc def            | 创建压缩包 用gzip命令压缩 将def文件压缩为名为abc的压缩包（也可以压缩目录） |
|         | 解压                                     | tar xzf abc -C aaa         | 将压缩包abc解压到aaa目录里去 用gzip解压                      |
| man     |                                          |                            |                                                              |
| echo    | 覆盖型写法 (原来内容被覆盖)              | echo 122 > 1.txt           | 将1.txt中的内容替换为122                                     |
|         | 添加型写法 (新内容添加在原来内容的后面） | echo abc >> 1.txt          | 输出为                                               122                                              abc |
|         |                                          |                            |                                                              |
|         |                                          |                            |                                                              |

#### &nbsp; 快捷键

---

1. ``Ctrl + C``：中断当前正在运行的命令。

2. ``Ctrl + Z``：将当前正在运行的命令放入后台。

3. ``Ctrl + P``：重复上一条指令。

4. Ctrl + D：在命令行中输入EOF（End of File）。

5. Ctrl + L：清屏，相当于执行"clear"命令。

6. Ctrl + A：将光标移动到命令行的开头。

7. Ctrl + E：将光标移动到命令行的末尾。

8. Ctrl + K：删除光标位置到行末的内容。

9. Ctrl + U：删除光标位置到行首的内容。

10. Ctrl + W：删除光标前的一个单词。

11. Ctrl + R：在历史命令中进行反向搜索。

12. Ctrl + G：退出历史命令搜索模式。

13. Tab键：自动补全命令或文件名。

    &emsp; 

#### &nbsp; vi命令

---

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214416324.png" width="500"/>
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



**编辑**  

&emsp;插入:输入i进入编辑模式  
&emsp;删除:  
&emsp;x:删除-一个字母  
&emsp;dw: del word  
&emsp;D:删除光标之后的内容  
&emsp;dd:删除整行  
&emsp;ndd //删除当前行及其后的n-1行(n是数字)  
&emsp;o:在当前行下面新增加--行  
&emsp;u:撤销上一-步操作  

**复制/粘贴**  

&emsp;yy:复制当前行(y:yank(复制))   
&emsp;nyy:复制当前行及其后的n-1 行(n是数字)  
&emsp;p:粘贴(p :paste)  

**查找/替换**  

&emsp;/pattern: 从光标开始处向文件尾搜索pattern, 后按下n(向下查找)或N(向上查找)  
&emsp;:8s/p1/p2/g :将文件中所有的p1均用p2替换  
&emsp;:8s/p1/p2/gc :替换时需要确认  

**测试NAT网卡能不能用：**

&emsp;利用ping www.baidu.com 测试
&emsp;不行的话 打开服务，把关于VMware的所有服务都启动

**用Source insight 来阅读源码(要破解，有点麻烦，我选择VScode)**

**Mount命令录制宏**

&nbsp;&emsp;  

&emsp;  

### 📉gcc编译器

---

#### 1、编译过程

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214648625.png" width="500"/>

**编译多个文件**

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



#### **2、制作和使用动态库、静态库**

静态库和动态库是两种常见的库类型，它们的主要区别在于代码被载入的时刻不同。

**静态库**是指在程序编译时被链接到目标代码中，一旦链接完成，最终的可执行程序中就包含了该库文件中的所有有用信息，包括代码段、数据段等。因此，静态库的体积较大。

**动态库**则是在程序执行时才被载入，因此程序运行的时候还需要动态库的存在。由于动态库在程序编译的时候不会被连接到目标代码，因此其代码的体积相对较小。

无论是静态库还是动态库，它们在功能上是没有区别的。但相对于动态库，静态库的优点在于其直接被链接进可执行程序中，因此该可执行程序就不再依赖于运行环境的设置了。而动态库的优点在于，用户甚至可以在程序运行时随时替换动态库，这就构成了动态插件系统的基础。

在不同的操作系统下，静态库和动态库的后缀名也不同。在Windows平台下，静态库的后缀为.lib，动态库的后缀为.dll；*==在Linux平台下，静态库的后缀为.a，动态库的后缀为.so。==*



#### **3、一些很有用的选项**

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214654604.png" width="500"/>

&emsp;gcc -E main.c // 查看预处理结果，比如头文件是哪个
&emsp;gcc -E -dM main.c > 1.txt // 把所有的宏展开，存在 1.txt 里
&emsp;gcc -Wp,-MD,abc.dep -c -o main.o main.c // 生成依赖文件 abc.dep ，后面 Makefile 会用
&emsp;echo 'main(){}'| gcc -E -v - // 它会列出头文件目录、库目录(LIBRARY_PATH)

&nbsp;&emsp;  

### 📉Shell脚本

---

Shell脚本是一种类似于Windows环境下的批处理文件，但功能更加强大。它是一种用各类命令预先放入到一个文件中，方便一次性执行的一个程序文件，主要是方便管理员进行设置或者管理用的。Shell脚本使用了Linux/Unix下的命令。



##### Shell脚本的语法规则

使用的是**Shell语言**。

Shell脚本是一系列Shell命令的集合，可以自动化执行各种任务，例如文件处理、文本处理、程序启动等。Shell脚本通常使用Shell语言的语法和控制结构，如条件语句、循环语句、函数等。







##### 重定向

在Shell脚本中，重定向是指将命令或操作的输出结果从默认的标准输出（通常是终端屏幕）重定向到文件或其他输出设备。通过重定向，您可以将命令的输出保存到文件中，或将其传递给其他命令作为输入。

重定向操作使用特殊的符号和语法来实现。以下是常见的重定向操作符和用法：

1. `>`：将输出重定向到一个新文件，如果文件已存在，则会覆盖文件内容。例如：


```shell
echo "Hello World" > output.txt
```
这将把"Hello World"写入output.txt文件中，如果文件不存在，则会创建文件；如果文件已存在，则会覆盖原有内容。
2. `>>`：将输出追加到一个文件末尾，不会覆盖文件原有内容。例如：


```shell
echo "New content" >> output.txt
```
这将在output.txt文件的末尾添加"New content"，而不会影响文件原有的内容。
3. `2>`：将错误输出重定向到一个文件。例如：


```shell
command 2> error.txt
```
这将把command命令的错误输出写入到error.txt文件中。
4. `&>`：将标准输出和错误输出同时重定向到一个文件。例如：


```shell
command &> output.txt
```
这将把command命令的标准输出和错误输出都写入到output.txt文件中。
5. `<>`：将标准输出和错误输出同时重定向到一个文件，但在写入时会以追加模式进行。例如：


```shell
command <> output.txt
```
这将在output.txt文件的末尾同时追加标准输出和错误输出。

这些重定向操作符可以与命令一起使用，让Shell脚本更加灵活地处理输出结果，比如将输出保存到文件、进行日志记录或者传递给其他命令作为输入等。



### 📉Makefile

---

#### **1、最简单的**

```c
gcc -o test a.c b.c
```

查看编译的详细信息：

```c
gcc -o test a.c b.c -v
```

<font color=red>缺点</font>：修改一个文件再编译，会对所有的文件重新编译

#### **2、Makefile核心—规则**

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

#### **3、命令格式：`make [目标]`**

&emsp;&emsp;单独使用make命令，只执行第一个test命令，不会执行其他的。但使用make clean时只执行clean命令

**语法**：

**通配符**（若有很多文件，则使用）：

$@：表示目标

$<：表示第1个依赖文件

$^：表示所有依赖文件

```c
test : a.o b.o c.o
	gcc -o test $^
%.o : %.c
	gcc -c -o $@ $<
```



**假想目标（.PHONY）**：

```c
test : a.o b.o c.o
	gcc -o test $^
%.o : %.c
	gcc -c -o $@ $<

clean :
	rm *.o test
.PHONY : clean
```

**解释**：

​		我们的Makefile中有这样的目标：

```c
clean:
    rm -f $(shell find -name "*.o")
    rm -f $(TARGET)
```

​		如果当前目录下恰好有名为“clean”的文件，那么执行“make clean”时它就不会执行那些删除命令。

​		这时我们需要把“clean”这个目标，设置为“假想目标”，这样可以确保执行“make clean”时那些删除命令肯定可以得到执行。

​		使用下面的语句把“clean”设置为假想目标：

​		``.PHONY : clean``

&emsp; 

**即时变量、延时变量**：

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

&emsp; 

#### **4、Makefile的函数**

**程序：**

```c
A = a b c
B = $ (foreach f, $(A)，$(f).o)	//将A中的所有文件加上.o

C = a b c d/
D = $ (filter  %/, $(C) )	//找出在C中所有符合%/的文件
E = $ (filter-out  %/, $(C) )	//找出在C中所有不符合%/的文件

files = a.c b.c c.c d.c e.c abc
files2 = $ (wildcard  $(files) )	//取出files中处在的文件
dep_files = $ (patsubst %.c, %.d, $(files) )
    		//从files中取出所有文件，找出符合.c的文件，然后全部替换成.d文件
    
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

&emsp; 

**字符替换函数**：

$(subst a, b, text)    ==//注意空格，空格也会起作用==

在文本text中使用b替换每一处a

比如：$(subst ee, EE, feet on the street)

结果为：fEEt on the strEEt



**格式替换函数**：

$(patsubst pattern,replacement,text) 

寻找text中符合格式pattern的字，用replacement替换它们。pattern和replacement中可以使用通配符。

比如：

$(patsubst %.c, %.o, x.c.c bar.c)

结果为：x.c.o bar.o

&emsp; 

**查找函数**：

$(findstring find,in) 

在字符串`in’中搜寻`find’，如果找到，则返回值是`find’，否则返回值为空。

比如：

$(findstring a, a b c)

$(findstring a, b c)

结果：a和(空字符串)

&emsp; 

#### **5、通用Makefile的设计思想**

[链接](E:\learn\weidongshan_Linux\01_all_series_quickstart\04_嵌入式Linux应用开发基础知识\doc_pic\01.嵌入式Linux应用开发基础知识.docx)

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214706385.png" width="500"/>



&emsp; 

&emsp;



### 📉文件IO

---

#### 1、标准IO和系统IO

**二者的不同**：

​		系统IO是直接进入内核，标准IO是在系统IO上又封装了一层函数，它多了一个用户Butter，不用每次执行函数时都进入内核，而是进入用户Butter，提高了效率

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214713139.png" width="500"/>

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214720906.png" width="500"/>

把SD卡插到开发板上，挂载它的分区，然后去访问对应的目录就可以了

主设备号表示哪一个驱动，次设备号表示这个设备里面的哪一个硬件









#### 2、怎么访问文件?

**通用的IO模型**：open/read/write/lseek/close
**不是通用的函数**： ioctl/mmapl



#### 3、系统调用函数怎么进入内核？

 ![image-20230928214728331](https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214728331.png)

1、用户空间，通过各种函数去调用内核空间，

2、gibc系统调用的函数会设置异常的原因，将其存在某些地方，然后通过swi和sic汇编指令来触发异常

3、CPU发现异常，会调用内核处理异常的函数，然后分辨异常原因，处理异常





#### 4、**每个进程有自己的文件句柄空间**

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214743470.png" width="500"/>

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214753679.png" width="500"/>





#### 5、man手册

​		当使用某些函数时，如果不知道包含哪些头文件时，可以用man手册，比如``man open``，如果找不到则``man 2 open``		

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214801457.png" width="500"/>





既可以查看命令的用法，还可以查看函数的详细介绍

进入man手册后，输入``./abc321``可查看手册中关于"abc321"的内容，按n键查找下一项











#### 6、各种函数

**open函数**：

用open函数可以创建一个新的文件

可以自定义创建的文件属性，但有的权限不能改，是因为umask的权限保护

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214807351.png" width="500"/>



**write函数**：

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214815188.png" width="500"/>





**read函数**：

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214821495.png" width="500"/>

#### 7、零星知识点

`hexdump -C XXX.csv`

可以把文件以十六进制的形式打印出来

&emsp; 

### ==❓未弄懂的==

---

#### 1、文件从哪里来

<img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214830522.png" width="500"/>









#### 2、内核的sys_open、sys_read会做什么？

 <img src="https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214837019.png" width="500"/>

#### 3、Framebuffer的应用编程（LCD显示）

![image-20230929194253081](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230929194253081.png)

#### 4、交叉编译程序

![image-20230929211817565](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230929211817565.png)

### 📉文字及图像显示

![image-20230929201835850](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230929201835850.png)



### 📉多线程编程

---

​		**进程**可以看作是一家餐厅，而线程则是餐厅里的服务员。这家餐厅（进程）有自己的地址和空间，储存了所有的食物（数据）。每当有客人（新的进程）来餐厅吃饭时，餐厅（操作系统）就会为客人分配一个新的餐桌（内存空间），并且为客人准备食物（分配资源）。

​		服务员（线程）则在餐厅（进程）内部工作，他们共享餐厅的资源，比如食物（数据）和餐具（内存）。每个服务员都可以在自己的工作区域内为客人服务，并且可以使用餐厅内的公共区域，比如厨房（共享内存）。但是，如果有一个服务员正在使用厨房（访问共享内存），其他服务员就需要等待他使用完毕后才能使用。

​		这样，餐厅（进程）可以同时接待多个客人（运行多个线程），而每个客人都有自己的服务员（线程）为他们服务。服务员之间通过共享餐厅的资源来协同工作，完成客人的要求。

​		如果一个程序拥有**多线程**能力，意味着它能够在同一时间执行多个线程，进而提升整体处理性能。这就像餐厅里有很多服务员，他们可以同时为多个客人服务，从而提高了餐厅的工作效率。

---

#### 1、线程的使用流程		

​		首先需要创建线程，一旦线程创建完成后，线程与线程之间会发生竞争执行，抢占时间片来执行线程逻辑。在创建线程时候，可以通过创建线程的第四个参数传入参数，在线程退出时亦可传出参数被线程回收函数所回收，获取到传出的参数

<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231001211323802.png" alt="image-20231001211323802" style="zoom:33%;" />

**1）获取线程号**

```c
#include <pthread.h>
pthread_t pthread_self(void);
```


通过函数 pthread_self，来返回当前线程的线程号



**2）线程的创建函数**

```c
#include <pthread.h>
int pthread_create(pthread_t *thread, const pthread_attr_t *attr,void *(*start_routi
ne) (void *), void *arg);
```

⚫ 第一个参数为 pthread_t 指针，用来保存新建线程的线程号；
⚫ 第二个参数表示了线程的属性，一般传入 NULL 表示默认属性；
⚫ 第三个参数是一个函数指针，就是线程执行的函数。这个函数返回值为 void\*，形参为 void*
⚫ 第四个参数则表示为向线程处理函数传入的参数，若不传入，可用 NULL 填充，



**程序分析：**

```c
#include <pthread.h>
#include <stdio.h>
#include <unistd.h>
#include <errno.h>

void *fun(void *arg)	//这是一个线程函数，它接受一个void指针作为参数，并返回一个void指针。
{
	// 打印出当前线程的tid 号
    printf("pthread_New = %lu\n",(unsigned long)pthread_self());
}

int main()
{
    //定义一个pthread_t类型的变量tid1
	pthread_t tid1;	
	int ret = pthread_create(&tid1,NULL,fun,NULL);	//创建线程
	if(ret != 0)
	{
		perror("pthread_create");
		return -1;
	}
     //在主线程中打印主线程的ID和新创建的线程的ID。
	printf("tid_main = %lu tid_new = %lu \n",(unsigned long)pthread_self(),(unsigned long)tid1);
   //使主线程睡眠1秒。这是为了确保新创建的线程有时间运行并打印其ID。如果没有这个sleep语句，主线程可能在新线程开始运行之前就已经结束，导致你看不到新线程的输出。
	sleep(1);
    return 0;
}
```



**3）向线程传入参数**



**4）线程的退出与回收**

**线程主动退出**

```c
#include <pthread.h>
void pthread_exit(void *retval);

```

在退出时候可以传递一个 void*类型的数据带给主线程，若选择不传出数据，可将参数填充为NULL



**线程被动退出**
其他线程使用该函数让另一个线程退出

```c
#include <pthread.h>
int pthread_cancel(pthread_t thread);
```

该函数传入一个 tid 号，会强制退出该 tid 所指向的线程，若成功执行会返回 0



**线程资源回收( 阻塞方式)**

```c
#include <pthread.h>
int pthread_join(pthread_t thread, void **retval);
```

默认状态为阻塞状态，直到成功回收线程后才返回。第一个参数为要回收线程的 tid 号，第二个参数为线程回收后接受线程传出的数据



**线程资源回收( 非阻塞方式)**

```c
#define _GNU_SOURCE
#include <pthread.h>
int pthread_tryjoin_np(pthread_t thread, void **retval);
```


通过返回值判断是否回收掉线程，成功回收则返回 0，其余参数与 pthread_join 一致。





#### 2、互斥锁

​		当线程在运行过程中，去操作公共资源，如全局变量的时候，可能会发生彼此“矛盾”现象。例如线程 1 企图想让变量自增，而线程 2 企图想要变量自减，两个线程互相竞争，变量似乎永远在某个范围内浮动，无法到达期望数值

​		多个线程都要访问某个临界资源，比如某个全局变量时，需要互斥地访问：我访问时，你不能访问。这就用到了互斥锁

<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231001211515488.png" alt="image-20231001211515488" style="zoom: 50%;" />



**1）初始化互斥量**

```c
int pthread_mutex_init(phtread_mutex_t *mutex,
const pthread_mutexattr_t *restrict attr);
```

该函数初始化一个互斥量，第一个参数是改互斥量指针，第二个参数为控制互斥量的属性，一般为 NULL。当函数成功后会返回 0，代表初始化互斥量成功。
当然初始化互斥量也可以调用宏来快速初始化，代码如下：

```c
pthread_mutex_t mutex = PTHREAD_MUTEX_INITALIZER;
```


**2）互斥量加锁（阻塞）/ 解锁**

```c
#include <pthread.h>
int pthread_mutex_lock(pthread_mutex_t *mutex);
int pthread_mutex_unlock(pthread_mutex_t *mutex);
```

只需要传入已经初始化好的pthread_mutex_t 互斥量指针。成功后会返回 0。
当某一个线程获得了执行权后，执行 lock 函数，一旦加锁成功后，其余线程遇到 lock 函数时候会发生阻塞，直至获取资源的线程执行 unlock 函数后。unlock 函数会唤醒其他正在等待互斥量的线程。



**3）互斥量加锁（非阻塞）**

```c
#include <pthread.h>
int pthread_mutex_trylock(pthread_mutex_t *mutex);
```


该函数同样也是一个线程加锁函数，但该函数是非阻塞模式通过返回值来判断是否加锁成功，用法与上述阻塞加锁函数一致。



**4）互斥量销毁**

```c
#include <pthread.h>
int pthread_mutex_destory(pthread_mutex_t *mutex);
```


该函数是用于销毁互斥量的，传入互斥量的指针，就可以完成互斥量的销毁，成功返回 0



#### 3、信号量（多个线程执行顺序控制）

​		解决了临界资源的访问，因线程都是无序执行，我们似乎对线程的执行顺序无法得到控制，于是便引入了信号量的概念，解决线程执行顺序，就用到了信号量。信号量起通知作用，线程 A 在等待某件事，线程 B 完成了这件事后就可以给线程 A 发信号。

​		当多个线程出现后，同时会遇到无序执行的问题。有时候需要对线程的执行顺序做出限定，变引入了信号量，通过 PV 操作来控制线程的执行顺序。

<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231001211805874.png" alt="image-20231001211805874" style="zoom:33%;" />



**1）初始化信号量**

```c
int sem_init(sem_t *sem,int pshared,unsigned int value);
```

⚫ 该函数可以初始化一个信号量，第一个参数传入 sem_t 类型指针；
⚫ 第二个参数传入 0 代表线程控制，否则为进程控制；
⚫ 第三个参数表示信号量的初始值，0 代表阻塞，1 代表运行。
⚫ 待初始化结束信号量后，若执行成功会返回 0。



**2）信号量 P/V 操作**

```c
#include <pthread.h>
int sem_wait(sem_t *sem);
int sem_post(sem_t *sem);
```

⚫ sem_wait 函数作用为检测指定信号量是否有资源可用，若无资源可用会阻塞等待，若有资源可用会自动的执行“sem-1”的操作。所谓的“sem-1”是与上述初始化函数中第三个参数值一致，成功执行会返回 0。
⚫ sem_post 函数会释放指定信号量的资源，执行“sem+1”操作。通过以上 2 个函数可以完成所谓的 PV 操作，即信号量的申请与释放，完成对线程执行顺序的控制



**3）信号量申请( 非阻塞方式)**

```c
#include <pthread.h>
int sem_trywait(sem_t *sem);
```

功能与 sem_wait 一致，唯一区别在于此函数为非阻塞



**4）信号量销毁**

```c
#include <pthread.h>
int sem_destory(sem_t *sem);
```

执行过后可将信号量进行销毁



**5）举例**

​		初始化sem1有资源，sem2、sem3阻塞，  只有14行fun1执行了``sem_post(&sem2)``，才会释放sem2，才会使20行fun2中``sem_wait(&sem2)``执行



<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231001210510145.png" alt="image-20231001210510145" style="zoom: 33%;" />





---

v



查看进程和线程

<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231001115718512.png" alt="image-20231001115718512" style="zoom:50%;" />

杀死之前的进程：

<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231001120049488.png" alt="image-20231001120049488" style="zoom:50%;" />



将其进行后台执行

<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231001120120522.png" alt="image-20231001120120522" style="zoom: 80%;" />





使用top命令

<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231001120522186.png" alt="image-20231001120522186" style="zoom:50%;" />





#### 4、线程安全

什么是线程不安全？
多个线程访问同一块临界资源，导致资源产生二义性的现象。

6.1.1举一个例子
假设现在有两个线程A和B，单核CPU的情况下，此时有一个int类型的全局变量为100，A和B的入口函数都要对这个全局变量进行–操作。
线程A先拿到CPU资源后，对全局变量进行–操作并不是原子性操作，也就是意味着，A在执行–的过程中有可能会被打断。假设A刚刚将全局变量的值读到寄存器当中，就被切换出去了，此时程序计数器保存了下一条执行的指令，上下文信息保存寄存器中的值，这两个东西是用来线程A再次拿到CPU资源后，恢复现场使用的。
此时，线程B拿到了CPU资源，对全局变量进行了–操作，并且将100减为了99，回写到了内存中。
A再次拥有了CPU资源后，恢复现场，继续往下执行，从寄存器中读到的值仍为100，减完之后为99，回写到内存中为99。
上述例子中，线程A和B都对全局变量进行了–操作，全局变量的值应该变为98，但程序现在实际的结果为99，所以这就导致了线程不安全。


##### POSIX信号量

是一种实现进程/线程间同步或临界资源互斥访问的机制，常用于协助一组相互竞争的进程/线程来访问临界资源。

在POSIX标准中，信号量分两种：一种是无名信号量，一种是有名信号量。无名信号量一般用于进程/线程间同步或互斥，而有名信号量一般用于进程间同步或互斥。

1. 无名信号量直接保存在内存中，主要用于进程或线程间同步或互斥。
2. 有名信号量则要求创建一个文件，主要用于进程间同步或互斥。

以上内容仅供参考，可以咨询计算机领域专业人士获取更全面准确的信息。







#### 5、条件变量















### 📉网络编程

#### 1、网络编程的基本概念

![image-20230929215054299](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230929215054299.png)













#### 2、两种传输方式：TCP/UDP

**1、为何存在 UDP 协议，UDP 的优点：**





#### 3、网络编程主要函数

**socket 函数**	创建一个套接字
```int socket(int domain, int type,int protocol);```

**bind 函数	**将地址绑定到一个套接字
```int bind(int sockfd, struct sockaddr *my_addr, int addrlen);```

⚫ sockfd 是由 socket 函数调用返回的文件描述符。
⚫ my_addr 是一个指向 sockaddr 的指针。
⚫ addrlen 是 sockaddr 结构的长度。



**listen 函数**	宣告服务器可以接受连接请求
```int listen(int sockfd,int backlog);```
⚫ sockfd 是 bind 后的文件描述符。
⚫ backlog 设置请求排队的最大长度。当有多个客户端程序和服务端相连时，
使用这个表示可以介绍的排队长度。
⚫ listen 函数将 bind 的文件描述符变为监听套接字，返回的情况和 bind 一
样。



**accept 函数**	服务器使用此函数获得连接请求，并且建立连接。
```int accept(int sockfd, struct sockaddr *addr,int *addrlen);```
⚫ sockfd 是 listen 后的文件描述符。
⚫ addr ，addrlen 是用来给客户端的程序填写的,服务器端只要传递指针就可
以了， bind,listen 和 accept 是服务器端用的函数。
⚫ accept 调用时，服务器端的程序会一直阻塞到有一个客户程序发出了连接。
accept 成功时返回最后的服务器端的文件描述符，这个时候服务器端可以向该
描述符写信息了，失败时返回-1 。



**connect 函数**	可以用 connect 建立一个连接，在 connect 中所指定的地址是想与之通信的服
务器的地址。
```int connect(int sockfd, struct sockaddr * serv_addr,int addrlen);```

⚫ sockfd 是 socket 函数返回的文件描述符。
⚫ serv_addr 储存了服务器端的连接信息，其中 sin_add 是服务端的地址。
⚫ addrlen 是 serv_addr 的长度
⚫ connect 函数是客户端用来同服务端连接的.成功时返回 0，sockfd 是同服
务端通讯的文件描述符，失败时返回-1。



**send 函数**
```ssize_t send(int sockfd, const void *buf, size_t len, int flags);```
⚫ sockfd 指定发送端套接字描述符；
⚫ buf 指明一个存放应用程序要发送数据的缓冲区；
⚫ len 指明实际要发送的数据的字节数；
⚫ flags 一般置 0。
⚫ 客户或者服务器应用程序都用 send 函数来向 TCP 连接的另一端发送数据



**recv 函数**
```ssize_t recv(int sockfd, void *buf, size_t len, int flags);```
⚫ sockfd 指定接收端套接字描述符；
⚫ buf 指明一个缓冲区，该缓冲区用来存放 recv 函数接收到的数据；
⚫ len 指明 buf 的长度；
⚫ flags 一般置 0。
⚫ 客户或者服务器应用程序都用 recv 函数从 TCP 连接的另一端接收数据。



**recvfrom 函数**
```ssize_t recvfrom(int sockfd, void *buf, size_t len, int flags,```
										```										struct sockaddr *src_addr, socklen_t *addrlen);```
⚫ recvfrom 通常用于无连接套接字，因为此函数可以获得发送者的地址。
⚫ src_addr 是一个 struct sockaddr 类型的变量，该变量保存源机的 IP
地址及端口号。
⚫ addrlen 常置为 sizeof （struct sockaddr）。



**sendto 函数**
```ssize_t sendto(int sockfd, const void *buf, size_t len, int flags,```
									```const struct sockaddr *dest_addr, socklen_t addrlen);```
⚫ sendto 和 send 相似，区别在于 sendto 允许在无连接的套接字上指定一个目标地址。
⚫ dest_addr 表示目地机的 IP 地址和端口号信息，
Hardware Development Manual
⚫ addrlen 常常被赋值为 sizeof （struct sockaddr）。
⚫ sendto 函数也返回实际发送的数据字节长度或在出现发送错误时返回-1。

### 

### 📉串口编程

<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231003202727570.png" alt="image-20231003202727570" style="zoom:30%;" />

<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231003202752177.png" alt="image-20231003202752177" style="zoom:33%;" />

<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231003202813748.png" alt="image-20231003202813748" style="zoom:33%;" />

#### 1、TTY体系中设备节点的差别

**傻傻分不清**
/dev/ttyS0、/devttySAC0、 /dev/tty. /dev/tty0、 /dev/ty1、 /dev/console

它们有什么差别?



TTY/Terminal/Console/UART

它们有什么差别?







**/dev/ttyN(N=1,2,3...)**

Ctrl+Alt+FN(N=1,2,3...)，可分别打开不同终端

其中tty0表示串口，tty1、2、3表示不同虚拟终端

/dev/ty3、/dev/tty4: 表示某个程序使用的虚拟终端
//在tty3、 tty4终端来回切换，执行命令

```c
echo he1lo > /dev/tty3
echo hi    > /dev/tty4
```



**Terminal和Console的差别**

Terminal含有远端的意思，中文为:终端。Console翻译为控制台， 可以理解为权限更大、能查看更多信息。
比如我们可以在Console.上看到内核的打印信息，从这个角度上看:
Console是某一个Terminal
●Terminal并不都是Console。
●我们可以从多个Terminal中选择某一个作为Console
●很多时候，两个概念混用，并无明确的、官方的定义



**/dev/console**

选哪个?内核的打印信息从哪个设备上显示出来?
可以通过内核的cmdline来指定,
比如: console=ttyS0 console=tty
我不想去分辨这个设备是串口还是虚拟终端，
有没有办法得到这个设备?
有!通过/dev/console!
console=ttyS0时: /dev/console就是ttyS0
console=tty时: /dev/console就是前台程序的虚拟终端
console=tty0时: /dev/console就是前台程序的虚拟终端
console=ttyN时: /dev/console就是/dev/ttyN
console有多个取值时，使用最后- -个取值来判断



#### 2、TTY驱动程序框架

行规程的引入

#### 





### 📉I2C应用编程

#### SMBus协议

SMBus是I2C协议的一-个子集
SMBus: System Management Bus,系统管理总线。
SMBus最初的目的是为智能电池、充电电池、其他微控制器之间的通信链路而定义的。
SMBus也被用来连接各种设备，包括电源相关设备，系统传感器，EEPROM通讯设备等等。
SMBus为系统和电源管理这样的任务提供了一条控制总线，使用SMBus的系统，设备之间发送和接收消息都是
通过SMBus,而不是使用单独的控制线，这样可以节省设备的管脚数。
SMBus是基于I2C协议的，SMBus要求更严格, SMBus是I2C协议的子集。
<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231005210946157.png" alt="image-20231005210946157" style="zoom: 50%;" />



#### I2C系统的重要结构体



#### I2C_Tools

无需编写驱动直接访问设备

















### 📉系统编程

##### 进程的基本知识

在操作系统和编程中，PID、UID和PPID是进程控制和识别的重要标识符。

**PID**（进程标识符）是**Process Identifier**的缩写，它是操作系统中每个进程的唯一标识符。在运行时，系统会为每个打开的程序分配一个PID，通过PID可以唯一地标识一个进程。当进程终止后，其PID会被系统回收，可能会被分配给其他新运行的程序。

**UID**（用户标识符）也是用于标识和识别系统用户账号的数字或字母组合。在Linux系统中，UID通常是1-999之间的整数，其中0是超级用户。

**PPID**（父进程标识符）是**Process Parent Identifier**的缩写，代表当前进程的父进程ID。在计算机中，每个进程都有一个父进程，通过PPID可以找到一个进程的父进程。

这些标识符在操作系统、编程和系统管理中扮演着重要角色，用于进程控制、系统管理和资源分配等方面。







##### ps命令：

ps命令是Linux系统中的一个常用命令，用于显示当前活动进程的快照，可以提供进程的各种信息，例如进程的PID、CPU使用率、内存使用率等等。

以下是ps命令常用的用法和选项：

1. ps命令的基本用法：


```c
ps [options]
```
其中，options是可选的参数，可以用来指定需要显示的信息和格式。

2. ps命令的选项：


```c
-e：显示所有进程，包括其他用户的进程。
-f：显示完整的进程信息。
-l：使用长格式显示进程信息。
-u：以用户为主的格式来显示进程信息。
-t<终端机编号>：指定终端机编号，并列出属于该终端机的程序的状况。
```
3. ps命令的组合使用：


```c
ps -ef|grep xxxxxxxx：列出所有进程，并过滤出包含指定字符串的进程。
ps -t<终端机编号> -ef|grep xxxxxxxx：在指定终端机下，列出包含指定字符串的进程。
```
在使用ps命令时，可以灵活运用这些选项和组合，以获取需要的信息和格式。同时，还可以通过管道和grep命令结合使用，过滤出需要显示的进程信息。



##### 子进程的创建

利用fork函数：

![image-20231024160424657](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231024160424657.png)





##### 进程的状态

1. 创建状态（CREATED）：进程正在创建过程中，尚未分配到处理器或资源。
2. 就绪状态（READY）：进程已经获得除CPU之外的所有必需资源，并等待获得CPU以执行。
3. 运行状态（RUNNING）：进程正在CPU上执行。
4. 阻塞状态（BLOCKED）：进程正在等待某个事件（如等待I/O操作完成）而暂停运行。即使CPU空闲，该进程也不能运行。
5. 等待状态（WAITING）：进程正在等待特定条件成立才能继续运行。
6. 终止状态（TERMINATED）：进程已经结束执行并释放了大部分资源。
7. 挂起状态（SUSPENDED）：进程被挂起，暂停执行。这通常是为了调试或其他原因。

除了上述状态外，还可以根据进程的优先级和调度策略分为优先级高的进程和优先级低的进程。这些状态的划分有助于操作系统更好地管理和调度进程的执行。

**僵死状态**（Zombie state）是**进程已结束，但父进程尚未读取其退出状态时**的一种状态。

当子进程退出，父进程需要读取其退出状态以进行后续处理。如果父进程没有及时读取子进程的退出状态，子进程就会进入僵死状态。僵死状态的进程已经放弃了几乎所有的内存空间，没有任何可执行代码，也不能被调度，仅仅在进程列表中保留一个位置，记载该进程的退出状态等信息供其父进程收集。

总的来说，只要子进程退出，父进程还在运行，但父进程没有读取子进程状态，子进程就会进入僵死状态。





##### 进程间的通信

进程间通信（IPC，Inter-Process Communication）是指在不同进程之间传递数据和信息的技术。以下是一些常见的进程间通信方式：

1. 管道（Pipe）：管道是最基本的进程间通信方式之一，它分为无名管道PIPE和命名管道FIFO。匿名管道是只能单向传递数据的管道，命名管道则可以在不相关的两个进程之间进行通信。
2. 信号（Signal）：信号是一种异步的通信方式，用于通知一个进程某个事件已经发生。信号传递的信息比较简单，主要用于通知进程某个时间已经发生。
3. 消息队列（Message Queue）：消息队列是一种在进程之间传递数据的机制，它可以在不同进程之间传递数据和消息。
4. 共享内存（Shared Memory）：共享内存是一种高效的进程间通信方式，它可以让不同进程访问同一块内存空间。
5. 套接字（Socket）：套接字是一种可以在不同主机之间进行通信的进程间通信方式。它不仅仅可以用于本地进程通信，还可以用于不同主机之间的进程通信。

以上是一些常见的进程间通信方式，不同的通信方式适用于不同的应用场景，可以根据实际需要进行选择。





























### 📉驱动内核



