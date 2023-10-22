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