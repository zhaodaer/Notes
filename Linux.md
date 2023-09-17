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

### 学习方法
* 你现在已经有了一些Linux的基础了，应该系统学一下了
* 先把韦东山嵌入式Linux完整看一遍(不要全看，挑着看  
* 看经典书籍（鸟哥的Linux私房菜很不错）
* 看大佬们的有关源码   
* 找2-3个相关项目巩固一下，最好能写在简历上 
* 刷题   

#### 未解决的问题
1、Windows下ipconfig出问题了  
2、Mobaxterm不能远程登录Ubuntu  


#### 第一节
* 绝对路径用 \   相对路径用 /
* Shell命令  PATH环境变量设置
* ./ 表示当前目录下行命令  
* 在Linux系统中，每个设备都被当成一个文件来对待，例如SATA接口的硬盘文件名为 /dev/sd[a-d]  
* 绝对路径进入 cd /home/alien  
* 相对路径进入 cd ./XXX/  


### 📉基础命令

| 命令   | 意义                |                    用法            | 说明             |
| ------ | ------------------- |--------------------------------   | ---------------- |
| pwd    |                      |                                  |     显示当前目录   | 
| cd      |                     | cd ..                             | 上一级目录        |
|        |                       |cd ~                             |  进入家目录       |
|        |                      | cd -                               |  切回上一次操作的目录    |
| cp      |                     | cp a b                            |  将a复制一份命名为b        |
| ls       |                  | ls -l                               | 查看文件的属性权限             |
| mkdir    |                    |                                   | 创建目录        |
| rmdir   |                       |                                  |删除目录 （只能删除空目录）     |
| rm       |                     |rm -rf <目录路径>                   |         |
|  echo   |                    | echo abc > 1.1.txt                | 创建一个文件     |
| cat       |                    |                                | 列出文件的内容    |
| touch a       |              |touch a                           | 摸一下该文件，只改时间，不改内容    |
| mv   |                          |mv a ../                          |  将a移动到上一级目录里  |
|      |                            |    mv ../a .                   |  将上一级目录里的a移动到当前目录  |
| tab键    |                       |                               |tab键  补全当前目录下的文件名    |
| chmod   |                       |              chmod 675 <某个文件>            | 改变文件的权限（拥有者、同组其他用户和其他用户的可读r、可写w、可执行r等）  |
|     |                            |chmod -x <某个文件>                         |  权限全部去掉    |
|  chowm |改变文件的所有者           |   chown root root <某个文件>              |改变文件的拥有者、其他用户等   |
| root |                             |                            | 用户切换、登录、设置密码（不建议用  |
| sudo   |                            |                           | 临时切换为root用户  这个命令nb  |
| find |                             |    find abc -name *.1.txt                        | 指定当前目录下的abc文件夹下查找名字为1.1.txt、2.1.txt等文件 |
| grep   |                            |    grep "xyz" * -nwr             | 递归查找当前目录下的所以文件中含有xyz字符的文件  |
| tar  |   压缩                 |     tar czf abc def              |  创建压缩包 用gzip命令压缩 将def文件压缩为名为abc的压缩包（也可以压缩目录） |
|     |    解压                |     tar xzf abc -C aaa            | 将压缩包abc解压到aaa目录里去 用gzip解压  |

### 📉vi命令
![image](https://github.com/zhaodaer/Notes/assets/141413040/0ef785b2-29ad-425a-b9b7-d1534f6e392d)
保存退出        :wq  
不保存退出       :q!  
:set number   显示行号  
:set nonumber   不显示行号  
:256  跳到第256行  
ctrl+f  向前翻页  
ctrl+b  向后翻页  
G:跳到文件结尾  
0:跳到行首  
$:跳到行尾  

#### 编辑  
插入:输入i进入编辑模式  
删除:  
x:删除-一个字母  
dw: del word  
D:删除光标之后的内容  
dd:删除整行  
ndd //删除当前行及其后的n-1行(n是数字)  
o:在当前行下面新增加--行  
u:撤销上一-步操作  

#### 复制/粘贴  
yy:复制当前行(y:yank(复制))   
nyy:复制当前行及其后的n-1 行(n是数字)  
p:粘贴(p :paste)  

#### 查找/替换  
/pattern: 从光标开始处向文件尾搜索pattern, 后按下n(向下查找)或N(向上查找)  
:8s/p1/p2/g :将文件中所有的p1均用p2替换  
:8s/p1/p2/gc :替换时需要确认  


#### 测试NAT网卡能不能用：
利用ping www.baidu.com测试
不行的话 打开服务，把关于VMware的所有服务都启动



