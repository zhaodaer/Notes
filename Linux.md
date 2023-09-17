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


#### 第一节
* 绝对路径用 \   相对路径用 /
* Shell命令  PATH环境变量设置
* ./ 表示当前目录下进行操作

### 📉Java

| 命令   | 题目                                                                                                                         | 来源             |
| ------ | ---------------------------------------------------------------------------------------------------------------------------- | ---------------- |
| pwd   |                                                                              | 显示当前目录    |
| cd   | cd ..                                                                             | 上一级目录         |
|      | cd ~                                                                      |  进入家目录       |
|      | cd -                                                          |  切回上一次操作的目录          |

| Java   | [Java Map 中那些巧妙的设计](https://mp.weixin.qq.com/s/7UTEHA6pdHeitg1htzdcRw)                                               | 阿里技术团队     |
| Java   | [JDK 16 中的 ZGC：平均暂停时间 0.05 毫秒](https://zhuanlan.zhihu.com/p/359249269?)                                           | Glavo            |
| Java   | [再谈 synchronized 锁升级](https://mp.weixin.qq.com/s/G4z08HfiqJ4qm3th0KtovA)                                                | 码农参上         |
| Java   | [Java 线程池源码解析](https://juejin.cn/post/6946087172143317023)                                                            | Xiao 镔          |
| Java   | [String 的不可变真的是因为 final 吗？](https://www.cnblogs.com/cswiki/p/14628286.html)                                       | 飞天小牛肉       |
| Java   | [假期后来一波干货：一文理清 JVM 和 GC](https://www.toutiao.com/a6947938522997342734/)                                        | Java 架构师联盟  |


在Linux系统中，每个设备都被当成一个文件来对待，例如SATA接口的硬盘文件名为 /dev/sd[a-d]  
绝对路径进入 cd /home/alien  
相对路径进入 cd ./XXX/  
    
    
./ 当前目录  
 

tab键  补全当前目录下的文件名  
创建目录 mkdir   
创建一个文件 echo abc > 1.1.txt  
删除目录 rmdir（只能删除空目录）  
删除命令 rm -rf <目录路径>  
cp a b     将a复制一份命名为b  
mv a ../    将a移动到上一级目录里  
mv ../a .    将上一级目录里的a移动到当前目录  
cat     列出文件的内容  
touch a  摸一下该文件，只改时间，不改内容  
ls -l  查看文件的属性权限  
改变文件的权限（拥有者、同组其他用户和其他用户的可读r、可写w、可执行r等）  chmod 675 <某个文件>    

sudo 临时切换为root用户  这个命令nb  
chmod -x <某个文件>     权限全部去掉  
chowm  改变文件的所有者    chown root root <某个文件>  改变文件的拥有者、其他用户等  
root用户切换、登录、设置密码（不建议用）  


find命令  find abc -name *.1.txt    指定当前目录下的abc文件夹下查找名字为1.1.txt、2.1.txt等文件  
grep命令  grep "xyz" * -nwr    递归查找当前目录下的所以文件中含有xyz字符的文件  



压缩命令 tar czf abc def  创建压缩包 用gzip命令压缩 将def文件压缩为名为abc的压缩包（也可以压缩目录）  
解压命令 tar xzf abc -C aaa    将压缩包abc解压到aaa目录里去 用gzip解压  





