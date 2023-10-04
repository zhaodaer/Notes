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

<h1 style="border:2px solid Tomato;">Hello World</h1>
边框颜色

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







## 三种使用 CSS 的方法

有三种插入样式表的方法：

- 外部 CSS

  通过使用外部样式表，您只需修改一个文件即可改变整个网站的外观！

  每张 HTML 页面必须在 head 部分的 <link> 元素内包含对外部样式表文件的引用。

- 内部 CSS

  如果一张 HTML 页面拥有唯一的样式，那么可以使用内部样式表。

  内部样式是在 head 部分的 <style> 元素中进行定义。

- 行内 CSS

  行内样式（也称内联样式）可用于为单个元素应用唯一的样式。

  如需使用行内样式，请将 style 属性添加到相关元素。style 属性可包含任何 CSS 属性。



**注意：**

当为某个 HTML 元素指定了多个样式时，会使用哪种样式呢？

页面中的所有样式将按照以下规则“层叠”为新的“虚拟”样式表，其中第一优先级最高：

1. 行内样式（在 HTML 元素中）
2. 外部和内部样式表（在 head 部分）
3. 浏览器默认样式

因此，行内样式具有最高优先级，并且将覆盖外部和内部样式以及浏览器默认样式。













## CSS background - 简写属性

使用简写属性在一条声明中设置背景属性：

```
body {
  background: #ffffff url("tree.png") no-repeat right top;
}
```

在使用简写属性时，属性值的顺序为：

- background-color
- background-image
- background-repeat
- background-attachment
- background-position

属性值之一缺失并不要紧，只要按照此顺序设置其他值即可。请注意，在上面的例子中，我们没有使用 background-attachment 属性，因为它没有值。



## CSS Border - 简写属性

为了缩减代码，也可以在一个属性中指定所有单独的边框属性。

`border` 属性是以下各个边框属性的简写属性：

- `border-width`
- `border-style`（必需）
- `border-color`

### 实例

```css
p {
  border: 5px solid red;
}
```





## Margin - 简写属性

如果 `margin` 属性有四个值：

- margin: 25px 50px 75px 100px;

- - 上外边距是 25px
  - 右外边距是 50px
  - 下外边距是 75px
  - 左外边距是 100px

### 

如果 `margin` 属性设置三个值：

- margin: 25px 50px 75px;

- - 上外边距是 25px
  - 右和左外边距是 50px
  - 下外边距是 75px



如果 `margin` 属性设置两个值：

- margin: 25px 50px;

- - 上和下外边距是 25px
  - 右和左外边距是 50px



如果 `margin` 属性设置了一个值：

- margin: 25px;

- - 所有四个外边距都是 25px

