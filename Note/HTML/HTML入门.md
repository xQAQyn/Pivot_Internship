# HTML笔记

## HTML简介

- HTML是什么？
  - HTML(**H**yper**t**ext **M**arkup **L**anguage)是是一种用来结构化 Web 网页及其内容的标记语言。
- HTML不是什么？
  - HTML不是编程语言。
- HTML由什么组成？
  - 由一系列**元素**组成。

## 元素

```html
<p>C is best language in the world!</p>
```

- 以上为一个元素，主要有以下主要部分：
  - 开始标签：一个形如`<...>`的东西，标志着一个元素的开始。（`...`是元素名称以及属性）
  - 结束标签：一个形如`<\...>`的东西，标志着元素的结束。(`...`是元素的名称)
  - 内容：夹在两个标签之间的就是内容。

### 属性

- 一个元素也可以有属性，格式为`属性名="属性值"`，例如

```html
<p class="editor-note">阿巴阿巴阿巴</p>
```

### 嵌套元素

- HTML支持元素进行嵌套，例如

```html
<p>My cat is <strong>angry</strong> </p>
```

- 但需要保持嵌套顺序正确，下面为一错误例子：

```html
<p>My cat is <strong>angry</p></strong>
```

### 空元素

- 元素也可以没有内容，没有内容就叫空元素，空元素既没有内容也没有结束标签，例如

```html
<img src="images/logo.png" alt="test">
<!--作用是嵌入一个图像，其不需要内容-->
```

## HTML文档

首先给出一个示例HTML文档：

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title> Test Page </title>
    </head>
    <body>
        <img src="images/logo.jpg" alt="test">
    </body>
</html>
```

它包含以下几个部分：

- `<!DOCTYPE html>`：标识文档类型，保证文档正常被读取
- `<html>...</html>`：html元素，该元素包含整个界面，称为根元素
- `<head>...</head>`：head元素，该元素对用户不可见
- `<mata charset="utf-8">`：指明使用UTF-8进行编码~实际上咱一般也不用其它字符集~
- `<title>...</title>`：title元素，设置页面标题，显示在浏览器标签页上，也作为收藏网页的描述文字。
- `<body>...</body>`：body元素，包含期望让用户访问时看见的内容.

### 图像

示例：

```html
<img src="images/logo.png" alt="test">
```

- src为图像文字路径
- alt为描述文本，在图像**不可见**的时候出现，例如
  - 用户有视觉障碍，可以通过屏幕阅读器阅读alt内容
  - 当图像发生错误无法显示时，显示图像的位置将会显示alt内容

### 标记文本

#### 标题(Heading)

- 标题用于标记内容的标题和子标题
- html最多支持**6层**标题
- 格式：

```html
<h1>heading</h1>
<h2>subheading</h2>
```

#### 段落(Paragraph)

- 用于常规文本内容
- 格式：

```html
<p>context</p>
```

#### 列表(List)

- 常用列表类型：
  - 有序列表(Ordered List)，用`<ol>`包围
  - 无序列表(Unordered List)，用`<ul>`包围
- 对每一个列表项目(List Item)，用`<li>`包围
- 示例：

```html
<p>html的元素由以下几个部分组成</p>
<ul>
    <li>开始标志</li>
    <li>结束标志</li>
    <li>内容</li>
</ul>
```

### 链接(Anchor)

- 格式：`<a>...</a>`，表示为`...`添加链接
- 如果添加一个网络链接，则可以使用如下格式

```html
<a href="https://www.pivotstudio.cn/">Pivot Studio</a>
```

(href为超文本引用(**H**ypertext **Ref**erence)的缩写)

