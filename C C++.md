C++基础入门
》1C++初识
2 数据类型
2.1 整型
2.2 sizeof关键字
2.3 实型(浮点型)
2.4 字符型
2.5 转义字符
2.6 字符串型
2.7 布尔类型 bool
2.8 数据的输入
》3 运算符
》4 程序流程结构
5 数组"
6函数
7指针
>8 结构体



**强制类型转换**：（数据类型）变量名

例如：

```c++
char ch = 'a'

count << (int)ch << end1;	//打印命令，将字符型变量char型强制转换成int型
```



水平制表符\t:       8个空格，有利于对齐，整齐输出数据

![image-20230929173605629](C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20230929173605629.png)

C中的`\n `    =      C++中的`<< end1`

两个\输出一个\



 `const char *input = "42 1.23 Hello";` 

`const char *input` 声明了一个名为 `input` 的指针，该指针指向一个 `const char` 类型的值，即一个不可修改的字符。`= "42 1.23 Hello"` 是对 `input` 的初始化，它将 `input` 指向字符串常量 "42 1.23 Hello" 的首地址。





#### sscanf函数：

原型如下：


```c
int sscanf(const char *str, const char *format, ...);
```
其中：

* `str`是要解析的字符串。
* `format`是一个控制字符串，指定了如何读取和解析`str`中的数据。它可以包含格式说明符（如`%d`，`%f`，`%s`等），用于指定要读取的数据的类型和格式。
* `...`表示一个可变数量的附加参数，对应于`format`字符串中的格式说明符。这些参数将被填充为从`str`中读取的值。

`sscanf`函数返回成功读取和解析的项目数量。


```c
#include <stdio.h>

int main() {
    const char *input = "42 1.23 Hello";
    int number;
    double decimal;
    char word[100];
    
    int items_read = sscanf(input, "%d %lf %s", &number, &decimal, word);
    
    printf("Read %d items:\n", items_read);
    printf("Number: %d\n", number);
    printf("Decimal: %f\n", decimal);
    printf("Word: %s\n", word);
    
    return 0;
}
```
**输出**：


```c
Read 3 items:
Number: 42
Decimal: 1.230000
Word: Hello
```
在这个示例中，`sscanf`函数从字符串`"42 1.23 Hello"`中读取数据，并根据指定的格式`"%d %lf %s"`将数据填充到变量`number`，`decimal`和`word`中。然后，程序输出读取的项目数量和每个项目的值。







#### C 语言中指针和解引用：

1. 指针变量的声明和初始化：


```c
int a = 10;
int *p = &a; // 声明一个指向 int 类型的指针变量 p，并将其初始化为 a 的地址
```
在这个例子中，`p` 是一个指向 `int` 类型的指针变量，它存储了变量 `a` 的内存地址。

2. 通过指针访问变量的值：


```c
int a = 10;
int *p = &a;
printf("%d\n", *p); // 输出 10
```
在这个例子中，我们通过指针 `p` 访问了变量 `a` 的值，使用 `*p` 表示对指针 `p` 进行解引用操作，获取指针 `p` 所指向的值。

3. 通过指针修改变量的值：


```c
int a = 10;
int *p = &a;
*p = 20; // 修改 a 的值为 20
printf("%d\n", a); // 输出 20
```
在这个例子中，我们通过指针 `p` 修改了变量 `a` 的值。使用 `*p` 表示对指针 `p` 进行解引用操作，获取指针 `p` 所指向的变量的地址，然后将新的值存储在这个地址上。

4. 指针作为函数参数传递：


```c
void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x = 10, y = 20;
    swap(&x, &y); // 将 x 和 y 的地址作为参数传递给 swap 函数
    printf("%d %d\n", x, y); // 输出 20 10
    return 0;
}
```
在这个例子中，我们定义了一个 `swap` 函数，用于交换两个整数的值。函数的参数是两个指向整数的指针，函数内部通过解引用这些指针来访问和修改这些整数的值。在 `main` 函数中，我们将 `x` 和 `y` 的地址作为参数传递给 `swap` 函数，从而实现了两个整数的交换。