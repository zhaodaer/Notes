### 1、C++基础

面向对象：

类和对象、继承、重载、多态、数据封装、数据抽象、接口（抽象）

---

### 2、环境搭建

Windows 以及 Linux下编程

---

### 3、Qt Designer的基本使用

界面组成及配置

---

### 4、信号与槽

![image-20231103155816684](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231103155816684.png)

---

### 5、Qt控件

按钮：QPushButton、QTollButton、QRadioButton、QCheckBox

输入窗口：QLineEdit、QTextEdit、

显示窗口：QLabel、

容器：QScrollArea、QTollBox、QTabWidget、QFrame、QWidget

项目视图组：QListView、QTreeView、

项目控件组：QListWidget、QTableWidget































为什么需要设置父对象？

​			因为窗口需要互相联系，比如A需要显示在B上面，A需要指定B为父对象
​		设置父对象的两种方法:


```c++
// 1.通过构造函数传参
pushButton = new QPushButton(this);
// 2.通过setParent()方法
pushButton = new QPushButton;
pushButton->setParent(this);
```



Qt对象树机制，目的就是方便内存管理

![image-20231022220755102](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231022220755102.png)