```
<hr>  水平线
```

```
<br />  换行
```

```
<!-- This is a comment -->  注释
```

```
<h1>标题</h1>

<p>段落</p>
```





```
<h1 style="font-family:verdana">A heading</h1>   
标题字体为verdana
<p style="font-family:arial;color:red;font-size:20px;">A paragraph.</p>
段落字体为arial，颜色红，字号20px


<body style="background-color:yellow">
body背景颜色为黄
<h2 style="background-color:red">This is a heading</h2>
标题背景颜色为红
<p style="background-color:green">This is a paragraph.</p>
段落背景颜色为绿

<h1 style="text-align:center">This is a heading</h1>
标题居中
```





```

<b>This text is bold</b>    粗体

<strong>This text is strong</strong>  加重语气

<big>This text is big</big>   大号字

<em>This text is emphasized</em>  着重文字

<i>This text is italic</i>   斜体 

<small>This text is small</small>   小号字

<sub>subscript</sub>    下标

<sup>superscript</sup>   上标


<b>	定义粗体文本。
<big>	定义大号字。
<em>	定义着重文字。
<i>	定义斜体字。
<small>	定义小号字。
<strong>	定义加重语气。
<sub>	定义下标字。
<sup>	定义上标字。
<ins>	定义插入字。
<del>	定义删除字。
<s>	不赞成使用。使用 <del> 代替。
<strike>	不赞成使用。使用 <del> 代替。
<u>	不赞成使用。使用样式（style）代替。
```





<img src="C:\Users\东瑞\AppData\Roaming\Typora\typora-user-images\image-20231003130215876.png" alt="image-20231003130215876" style="zoom: 50%;" />







**通过使用 HTML4.0，所有的格式化代码均可移出 HTML 文档，然后移入一个独立的样式表。**



CSS 是一种描述 HTML 文档样式的语言。

CSS 描述应该如何显示 HTML 元素。



## 什么是 CSS？

- *CSS* 指的是层叠样式表* (*C*ascading *S*tyle *S*heets)
- CSS 描述了*如何在屏幕、纸张或其他媒体上显示 HTML 元素*
- CSS *节省了大量工作*。它可以同时控制多张网页的布局
- 外部样式表存储在 *CSS 文件*中

***：**也称级联样式表。

## CSS 节省了大量工作！

样式定义通常保存在外部 .css 文件中。

通过使用外部样式表文件，您只需更改一个文件即可更改整个网站的外观！



## CSS 语法

CSS 规则集（rule-set）由选择器和声明块组成：

![CSS 选择器](https://www.w3school.com.cn/i/css/selector.gif)

选择器指向您需要设置样式的 HTML 元素。

声明块包含一条或多条用分号分隔的声明。

每条声明都包含一个 CSS 属性名称和一个值，以冒号分隔。

多条 CSS 声明用分号分隔，声明块用花括号括起来。



### 实例

在此例中，所有 <p> 元素都将居中对齐，并带有红色文本颜色：

```
p {
  color: red;
  text-align: center;
}
```

### 解释

- `p` 是 CSS 中的*选择器*（它指向要设置样式的 HTML 元素：<p>）。
- `color` 是属性，`red` 是属性值
- `text-align` 是属性，`center` 是属性值









## CSS 元素选择器

元素选择器根据元素名称来选择 HTML 元素。

页面上的所有 <p> 元素都将居中对齐，并带有红色文本颜色：

```
p {
  text-align: center;
  color: red;
}
```



## CSS id 选择器

id 选择器使用 HTML 元素的 id 属性来选择特定元素。

元素的 id 在页面中是唯一的，因此 id 选择器用于选择一个唯一的元素！

要选择具有特定 id 的元素，请写一个井号（＃），后跟该元素的 id。

这条 CSS 规则将应用于 id="para1" 的 HTML 元素：

```
#para1 {
  text-align: center;
  color: red;
}
```

**注意：**id 名称不能以数字开头。



## CSS 类选择器

类选择器选择有特定 class 属性的 HTML 元素。

如需选择拥有特定 class 的元素，请写一个句点（.）字符，后面跟类名。

所有带有 class="center" 的 HTML 元素将为红色且居中对齐：

```
.center {
  text-align: center;
  color: red;
}
```

您还可以指定只有特定的 HTML 元素会受类的影响。

### 实例

在这个例子中，只有具有 class="center" 的 <p> 元素会居中对齐：

```
p.center {
  text-align: center;
  color: red;
}
```

HTML 元素也可以引用多个类。

### 实例

在这个例子中，<p> 元素将根据 class="center" 和 class="large" 进行样式设置：

```
<p class="center large">这个段落引用两个类。</p>
```

**注意：**类名不能以数字开头！



## CSS 通用选择器

通用选择器（*）选择页面上的所有的 HTML 元素。

### 实例

下面的 CSS 规则会影响页面上的每个 HTML 元素：

```
* {
  text-align: center;
  color: blue;
}
```



## CSS 分组选择器

分组选择器选取所有具有相同样式定义的 HTML 元素。

请看下面的 CSS 代码（h1、h2 和 p 元素具有相同的样式定义）：

```
h1 {
  text-align: center;
  color: red;
}

h2 {
  text-align: center;
  color: red;
}

p {
  text-align: center;
  color: red;
}
```

最好对选择器进行分组，以最大程度地缩减代码。

如需对选择器进行分组，请用逗号来分隔每个选择器。

### 实例

在这个例子中，我们对上述代码中的选择器进行分组：

```
h1, h2, p {
  text-align: center;
  color: red;
}
```



