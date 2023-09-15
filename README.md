![夜尽天明](https://upload-images.jianshu.io/upload_images/12890819-6e2289f29c0d3b39.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
# zhaodaer's Notebook

>**打不倒我的，只会让我更强大 ！**

    以技术笔记为主，记录自己平常学习到知识，以便以后查阅。  
    希望做一个终身学习者

## 计划
* 添加备忘录清单（reference）
* Docker的使用
<br>
<br>
<br>

## 一、[Linux](Linux.md)
>Linux虐我千百遍，我待Linux如初恋  
>这里的内容是我学习Linux的一些记录，希望能一直坚持下去

### 主要包括：
> * [环境配置](https://py3.io/doc/python/quickstart.html)
> * 基础语法
>   * XXX
>   * requests使用多IP请求
> * [应用开发](code/MultiThread_Template.py)
<br>
<br>
<br>

  
## 二、[数据结构和算法](数据结构和算法.md)
>算法虐我千百遍，我待算法如初恋  
>这些算法全部自己敲一遍：
### 大纲
> * [链表](https://py3.io/doc/python/quickstart.html)
> * 数组
>   * 数组数列问题
>   * requests使用多IP请求
>   * [Python多线程模板](code/MultiThread_Template.py)
> * 队列
>   * 队列
>   * 堆栈
> * 哈希表 HashTable
>   * 散列函数
>   * 碰撞解决
> * 字符串算法
>   * 子串查找 [字符串常见题目参考这里](9%20Algorithms%20Job%20Interview/1%20字符串.md) 
>   * BF算法  
>   * KMP算法  
>   * BM算法  
>   * 正则表达式
>   * 数据压缩
>   * 排序
> *  [树](4%20Tree/README.md)
>   * 二叉树  [快速排序](6%20Sort/README.md)就是个二叉树的前序遍历，归并排序就是个二叉树的后序遍历  
>   * [二叉查找树BST](4%20Tree/2-二叉查找树/二叉查找树.md)  有序的二叉树，中序遍历结果是递增的
>   * [平衡二叉树 AVL树](4%20Tree/3-平衡树AVL/README.md)   绝对平衡二叉树；
>   * [红黑树](4%20Tree/9-红黑树%20R-B%20tree/红黑树.md)  弱平衡二叉树；使用广泛
>   * [B树](4%20Tree/7-B树/B树.md)
>   * [B+树](4%20Tree/7-B树/B+树.md)  mysql 索引使用 B+树 的数据结构	  
>   * [字典树trie](4%20Tree/4-字典树Trie/README.md) 字典树也叫前缀树，单词查找树
>   * [二叉堆](4%20Tree/8-堆/堆.md)  
>   * [伸展树](4%20Tree/5-伸展树/伸展树.md)
>   * [后缀树](4%20Tree/6-后缀树/后缀树.md)
>   * 斐波那契堆(Fibonacci Heap)   
>   * 最优二叉树(赫夫曼树)  
> * [图的算法](5%20Graph/README.md)
>   * 图的存储结构和基本操作（建立，遍历，删除节点，添加节点）   
>   * 最小生成树  
>   * 拓扑排序  
>   * 关键路径  
>   * 最短路径: Floyd,Dijkstra,bellman-ford,spfa  
> * [排序算法](6%20Sort/README.md)
> * 交换排序算法
>   * 冒泡排序
>   * 插入排序    
>   * 选择排序    
>   * 希尔排序
>   * 快排   
>   * 归并排序  
>   * 堆排序
> * 线性排序算法
>   * 桶排序 
> * [查找算法](7%20Search/README.md)  
>   * 哈希表： O(1)  [hashtable实现参考这里](../3%20Hash%20Table/README.md)
>   * 有序表查找：二分查找 
>   * 顺序表查找：顺序查找, 复杂度O(N)  
>   * 分块查找： 块内无序，块之间有序；可以先二分查找定位到块，然后再到`块`中顺序查找  
>   * 动态查找:  二叉排序树，AVL树，B- ，B+（这里之所以叫 `动态查找表`，是因为表结构是查找的过程中动态生成的）
> * [算法设计思想](8%20Algorithms%20Analysis/README.md)
>   * [递归](8%20Algorithms%20Analysis/递归.md) 
>   * [分治算法](8%20Algorithms%20Analysis/分治算法.md) 
>   * [动态规划](8%20Algorithms%20Analysis/动态规划.md)  
>   * [回溯法](8%20Algorithms%20Analysis/回溯法.md)
>   * [迭代法](8%20Algorithms%20Analysis/迭代法.md)  
>   * [穷举搜索法](8%20Algorithms%20Analysis/穷举搜索法.md)   
>   * [贪心算法](8%20Algorithms%20Analysis/贪心算法.md) 
> * [面试算法题目](9%20Algorithms%20Job%20Interview/README.md)


<br>
<br>
<br>

        笔者觉得每个开发者都应该拥有自己的网站和服务器，这可是很酷的事情，学习 Linux、跑跑脚本、建站、搭博客啥的都行啊。
        因为笔者就有自己的服务器，而且有两台了，用于平时的学习，还搭建了自己的网站。
        有不少读者问过我，为什么我学的那么快的呢 ？ 怎么在一年内学了那么知识的...
        其实也没什么秘决，就是平时有自己的服务器了，就爱折腾，学到的知识能很快得到验证，所以学起来兴致高一点。
        特别是大三和大四的学生，买了服务器，搭建个项目给面试官看也香，对找工作和面试都加分
