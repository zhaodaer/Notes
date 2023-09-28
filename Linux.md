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

### 🥉碎碎念

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

![image-20230928214416324](https://raw.githubusercontent.com/zhaodaer/PicX/main/img/image-20230928214416324.png)
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

![image-20230922115433188](C:\Users\东瑞\Desktop\222\Notes\images\image-20230922115433188.png)

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

#### **3、一些很有用的选项**

![image-20230922122713220](C:\Users\东瑞\Desktop\222\Notes\images\image-20230922122713220.png)

&emsp;gcc -E main.c // 查看预处理结果，比如头文件是哪个
&emsp;gcc -E -dM main.c > 1.txt // 把所有的宏展开，存在 1.txt 里
&emsp;gcc -Wp,-MD,abc.dep -c -o main.o main.c // 生成依赖文件 abc.dep ，后面 Makefile 会用
&emsp;echo 'main(){}'| gcc -E -v - // 它会列出头文件目录、库目录(LIBRARY_PATH)

&nbsp;&emsp;  

### 📉Shell脚本

---

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

![image-20230925204013516](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230925204013516.png)



&emsp; 

&emsp;



### 📉文件IO

---

#### 1、标准IO和系统IO

**二者的不同**：

​		系统IO是直接进入内核，标准IO是在系统IO上又封装了一层函数，它多了一个用户Butter，不用每次执行函数时都进入内核，而是进入用户Butter，提高了效率

![image-20230925213741519](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230925213741519.png)

![image-20230925214002205](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230925214002205.png)

把SD卡插到开发板上，挂载它的分区，然后去访问对应的目录就可以了

主设备号表示哪一个驱动，次设备号表示这个设备里面的哪一个硬件









#### 2、怎么访问文件?

**通用的IO模型**：open/read/write/lseek/close
**不是通用的函数**： ioctl/mmapl



#### 3、系统调用函数怎么进入内核？

 ![image-20230925210458236](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230925210458236.png)

1、用户空间，通过各种函数去调用内核空间，

2、gibc系统调用的函数会设置异常的原因，将其存在某些地方，然后通过swi和sic汇编指令来触发异常

3、CPU发现异常，会调用内核处理异常的函数，然后分辨异常原因，处理异常





#### 4、**每个进程有自己的文件句柄空间**

![image-20230928165754778](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230928165754778.png)

![image-20230928165633331](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230928165633331.png)





#### 5、man手册

​		当使用某些函数时，如果不知道包含哪些头文件时，可以用man手册，比如``man open``，如果找不到则``man 2 open``		

![image-20230925214606340](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230925214606340.png)





既可以查看命令的用法，还可以查看函数的详细介绍

进入man手册后，输入``./abc321``可查看手册中关于"abc321"的内容，按n键查找下一项











#### 6、各种函数

**open函数**：

用open函数可以创建一个新的文件

可以自定义创建的文件属性，但有的权限不能改，是因为umask的权限保护

![image-20230926172236108](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230926172236108.png)



**write函数**：

![image-20230926174821293](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230926174821293.png)





**read函数**：

![image-20230926180821902](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230926180821902.png)

#### 7、零星知识点

`hexdump -C XXX.csv`

可以把文件以十六进制的形式打印出来

&emsp; 

### ==❓未弄懂的==

---

#### 1、文件从哪里来

![image-20230925210123776](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230925210123776.png)









#### 2、内核的sys_open、sys_read会做什么？

 ![image-20230925210505897](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230925210505897.png)



### 📉多线程编程

### 📉网络编程

### 📉I2C应用编程

### 📉驱动内核



