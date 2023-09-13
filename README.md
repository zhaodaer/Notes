

![夜尽天明](https://upload-images.jianshu.io/upload_images/12890819-6e2289f29c0d3b39.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


> **芳华正茂始少年，时光正好，未来可期 ！**

技术为主，读书笔记、随笔为辅，做个终身学习者。

收获不止技术，还有财富。

  

<!-- 
## 服务器

笔者觉得每个开发者都应该拥有自己的网站和服务器，这可是很酷的事情，学习 Linux、跑跑脚本、建站、搭博客啥的都行啊。

因为笔者就有自己的服务器，而且有两台了，用于平时的学习，还搭建了自己的网站。

有不少读者问过我，为什么我学的那么快的呢 ？ 怎么在一年内学了那么知识的...

其实也没什么秘决，就是平时有自己的服务器了，就爱折腾，学到的知识能很快得到验证，所以学起来兴致高一点。

特别是大三和大四的学生，买了服务器，搭建个项目给面试官看也香，对找工作和面试都加分



>Linux虐我千百遍，我待Linux如初恋

这里的内容是我学习Linux的一些记录，希望能一直坚持下去。

## 学习方法

* 你现在已经有了一些Linux的基础了，应该系统学一下了
* 先把韦东山嵌入式Linux完整看一遍(不要全看，挑着看  
* 看大佬们的有关源码   
* 找2-3个相关项目巩固一下，最好能写在简历上 
* 看经典书籍（鸟哥的Linux私房菜？）  
* 刷题   

## 1.添加备忘录清单（reference）

## 2.Docker的使用




### 笔记

#### 1、绝对路径用 \       相对路径用 /

#### 2、Shell命令  PATH环境变量设置

#### 3、./  表示当前目录下进行操作

## 基本数据结构和算法

这些算法全部自己敲一遍：

### [链表](2%20List/README.md)

* 链表
* 双向链表

### [数组](2%20List/数组.md)

* [数组数列问题](9%20Algorithms%20Job%20Interview/5%20数组数列问题.md)

数组和链表结构是基础结构，散列表、栈、队列、堆、树、图等等各种数据结构都基于数组和链表结构实现。

### [队列](2%20Queue/README.md)

* 队列
* 堆栈

### [哈希表 HashTable](3%20Hash%20Table/README.md)

* 散列函数
* 碰撞解决

### [字符串算法](1%20String/README.md)

* 子串查找 [字符串常见题目参考这里](9%20Algorithms%20Job%20Interview/1%20字符串.md) 
  * BF算法  
  * KMP算法  
  * BM算法  
* 正则表达式
* 数据压缩
* 排序


### [树](4%20Tree/README.md)

* 二叉树  [快速排序](6%20Sort/README.md)就是个二叉树的前序遍历，归并排序就是个二叉树的后序遍历  
* [二叉查找树BST](4%20Tree/2-二叉查找树/二叉查找树.md)  有序的二叉树，中序遍历结果是递增的
* [平衡二叉树 AVL树](4%20Tree/3-平衡树AVL/README.md)   绝对平衡二叉树；
* [红黑树](4%20Tree/9-红黑树%20R-B%20tree/红黑树.md)  弱平衡二叉树；使用广泛
* [B树](4%20Tree/7-B树/B树.md)
* [B+树](4%20Tree/7-B树/B+树.md)  mysql 索引使用 B+树 的数据结构	  
* [字典树trie](4%20Tree/4-字典树Trie/README.md) 字典树也叫前缀树，单词查找树
* [二叉堆](4%20Tree/8-堆/堆.md)  
* [伸展树](4%20Tree/5-伸展树/伸展树.md)
* [后缀树](4%20Tree/6-后缀树/后缀树.md)
* 斐波那契堆(Fibonacci Heap)   
* 最优二叉树(赫夫曼树)  



### [图的算法](5%20Graph/README.md)

* 图的存储结构和基本操作（建立，遍历，删除节点，添加节点）   

* 最小生成树  

* 拓扑排序  

* 关键路径  

* 最短路径: Floyd,Dijkstra,bellman-ford,spfa  

  

### [排序算法](6%20Sort/README.md)

**交换排序算法**

* 冒泡排序
* 插入排序    
* 选择排序    
* 希尔排序
* 快排   
* 归并排序  
* 堆排序

**线性排序算法**
    

* 桶排序 

  

### [查找算法](7%20Search/README.md)  


* 哈希表： O(1)  [hashtable实现参考这里](../3%20Hash%20Table/README.md)
* 有序表查找：二分查找 
* 顺序表查找：顺序查找, 复杂度O(N)  
* 分块查找： 块内无序，块之间有序；可以先二分查找定位到块，然后再到`块`中顺序查找  
* 动态查找:  二叉排序树，AVL树，B- ，B+（这里之所以叫 `动态查找表`，是因为表结构是查找的过程中动态生成的）


## [算法设计思想](8%20Algorithms%20Analysis/README.md)


* [递归](8%20Algorithms%20Analysis/递归.md) 
* [分治算法](8%20Algorithms%20Analysis/分治算法.md) 
* [动态规划](8%20Algorithms%20Analysis/动态规划.md)  
* [回溯法](8%20Algorithms%20Analysis/回溯法.md)
* [迭代法](8%20Algorithms%20Analysis/迭代法.md)  
* [穷举搜索法](8%20Algorithms%20Analysis/穷举搜索法.md)   
* [贪心算法](8%20Algorithms%20Analysis/贪心算法.md) 



## [面试算法题目](9%20Algorithms%20Job%20Interview/README.md)

这是一个算法题目合集，题目是我从网络和书籍之中整理而来，部分题目已经做了思路整理。问题分类包括：

* 字符串
* 堆和栈
* 链表
* 数值问题
* 数组和数列问题
* 矩阵问题
* 二叉树
* 图
* 海量数据处理
* 智力思维训练
* 系统设计

还有部分来自算法网站和书籍：

* 九度OJ
* leetcode
* 剑指offer


## [海量数据处理](91%20Algorithms%20In%20Big%20Data/README.md)

* Hash映射/分而治之
* Bitmap
* Bloom filter(布隆过滤器)
* Trie树
* 数据库索引
* 倒排索引(Inverted Index)
* 双层桶划分
* 外排序
* simhash算法
* 分布处理之Mapreduce



## [开源项目中的算法](93%20Algorithms%20In%20Open%20Source/README.md)

* YYCache
* cocos2d-objc
* bitcoin
* geohash
* kafka
* nginx
* zookeeper
* ...




## 15个经典基础算法


* [KMP 字符串匹配算法](1%20String/KMP.md)
* [Hash](3%20Hash%20Table/README.md)   
* [快速排序](6%20Sort/README.md)
* 快速选择SELECT 
* [红黑树 （一种弱/自平衡的`二叉查找树`）](4%20Tree/9-红黑树%20R-B%20tree/红黑树.md)
* [BFS/DFS （广度/深度优先遍历）](5%20Graph/DFS%20和%20BFS.md)
* [`A*`寻路算法： 求解最短路径](5%20Graph/最短路径.md)
* Dijkstra：最短路径算法
* `SPFA(Shortest Path Faster Algorithm)` 单元最短路径算法  
* 启发式搜索
* 遗传算法 `GA`  
* [DP (动态规划 dynamic programming)](8%20Algorithms%20Analysis/动态规划.md)
* 图像特征提取之`SIFT` 算法 , 广泛的应用于图像识别，图像检索，3D重建等CV的各种领域 
* 傅立叶变换  


## 推荐阅读

### 刷题必备  

* 《剑指offer》  
* 《编程之美》  
* 《编程之法:面试和算法心得》      
* 《算法谜题》 都是思维题 

### 基础

* 《编程珠玑》Programming Pearls   
* 《编程珠玑(续)》   
* 《数据结构与算法分析》   
* 《Algorithms》 这本近千页的书只有6章,其中四章分别是排序，查找，图，字符串，足见介绍细致     

### 算法设计 

* 《算法设计与分析基础》    
* 《算法引论》 告诉你如何创造算法   断货        
* 《Algorithm Design Manual》算法设计手册 红皮书  
* 《算法导论》 是一本对算法介绍比较全面的经典书籍     
* 《Algorithms on Strings,Trees and Sequences》    
* 《Advanced Data Structures》 各种诡异高级的数据结构和算法 如元胞自动机、斐波纳契堆、线段树  600块    

### 延伸阅读 

* 《深入理解计算机系统》    
* 《TCP/IP详解三卷》    
* 《UNIX网络编程二卷》  
* 《UNIX环境高级编程：第2版》  
* 《The practice of programming》   Brian Kernighan和Rob Pike    
* 《writing efficient programs》  优化   
* 《The science of programming》 证明代码段的正确性   800块一本   


## 参考链接和学习网站

### [July 博客](http://blog.csdn.net/v_july_v) 

* 《数学建模十大经典算法》    
* 《数据挖掘领域十大经典算法》    
* 《十道海量数据处理面试题》      
* 《数字图像处理领域的二十四个经典算法》    
* 《精选微软等公司经典的算法面试100题》 
* [The-Art-Of-Programming-By-July](https://github.com/julycoding/The-Art-Of-Programming-By-July)
* [微软面试100题](http://blog.csdn.net/column/details/ms100.html)    
* [程序员编程艺术](http://blog.csdn.net/v_JULY_v/article/details/6460494)   


### 基本算法演示 

http://sjjg.js.zwu.edu.cn/SFXX/sf1/sfys.html  
http://www.cs.usfca.edu/~galles/visualization/Algorithms.html  


### 编程网站

* [leetcode](http://leetcode.com/)   
* [codetop](https://codetop.cc/home) 企业高频面试题库，刷题必备
* [openjudge](http://openjudge.cn/)  开放在线程序评测平台，可以创建自己的OJ小组   
* [九度OJ](http://ac.jobdu.com/index.php)     
* 这有个[ACM训练方案](http://www.java3z.com/cwbwebhome/article/article19/res041.html)   


### 网课

[高级数据结构和算法](https://www.coursera.org/learn/gaoji-shuju-jiegou/)  北大教授张铭老师在coursera上的课程。完成这门课之时，你将掌握多维数组、广义表、Trie树、AVL树、伸展树等高级数据结构，并结合内排序、外排序、检索、索引有关的算法，高效地解决现实生活中一些比较复杂的应用问题。当然coursera上也还有很多其它算法方面的视频课程。


[算法设计与分析 Design and Analysis of Algorithms](https://class.coursera.org/algorithms-001/lecture) 由北大教授Wanling Qu在coursera讲授的一门算法课程。首先介绍一些与算法有关的基础知识，然后阐述经典的算法设计思想和分析技术，主要涉及的算法设计技术是：分治策略、动态规划、贪心法、回溯与分支限界等。每个视频都配有相应的讲义（pdf文件）以便阅读和复习。


### 其它

[OI Wiki](https://github.com/24OI/OI-wiki/) 主要内容是 OI/ACM-ICPC 编程竞赛 (competitive programming) 相关的知识整理, 包括基础知识、常见题型、解题思路以及常用工具等内容。

[labuladong 的算法小抄](https://labuladong.gitee.io/algo/) 作者整理了很多的解题套路框架，看完获益良多

## 联系

[@移动开发小冉](http://weibo.com/ranwj)

