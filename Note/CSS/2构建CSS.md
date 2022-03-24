# 构建CSS

## 在HTML中使用CSS

### 外部样式表

- 将CSS编写在单独的`.css`文件中，然后在HTML`<link>`引用，例如

```css
<link rel="stylesheet" href="styles.css">
```

此时CSS文件与HTML文档位于同一文件夹中，如果不在同一文件夹，可以使用路径，例如

```css
<link rel="stylesheet" href="styles/general/style.css">
```

### 内部样式表

- 可以直接将CSS放入HTML文件`<head>`中的`<style>`当中，例如

```html
<head>
    <style>
        p {
        	color: red;
      	}
    </style>
</head>
```

### 内联样式

- 可以直接将CSS放入元素的style属性之中，它只影响一个元素，

```html
<p style="color: blue;font-size: 5em">
    2333333
</p>
```

**注意**：一般不要使用该方式

## 选择器专一性

- 若同一个元素适用CSS中多个规则，最终采用的规则称为级联规则和专用规则
- 当对同一个元素定义多个规则时，将采取最后一个规则，例如

```css
p {
    color: red;
}
p{
    color: blue
}
/*最后<p>会渲染为蓝色*/
```

- 对一个带有类的元素，渲染时将优先采用类的规则，例如

```css
.xyn{
    color: red;
}
p{
    color: blue;
}
/*最后<p class="xyn">会被渲染为红色*/
```

## 属性和值

- CSS的每条规则由两个部分组成：属性、值

### 属性

- 属性：人类可读的标识符，代表你要修改的东西，常用属性有
  - `font-size`：字号
  - `width`：内容区域宽度
  - `background-color`：背景色（默认为`transparent`）
  - `color`：字体颜色
  - `border`：边框属性（包括宽度、颜色、风格等）

### 值

- 值：每个属性都有一个值，代表你更改属性的方式
- 值可以是简单的关键字或者数值，也可以是一个函数，例如`calc()`函数：

```html
<div class="outer"><div class="box">The inner box is 90% - 30px.</div></div>
```

```css
.outer {
  border: 5px solid black;
}

.box {
  padding: 10px;
  width: calc(90% - 30px);/*宽度为块宽的90%减去30个像素*/
  background-color: rebeccapurple;
  color: white;
}
```

还有`ronate()`函数：

```html
<div class="box"></div>
```

```css
.box {
  margin: 30px;
  width: 100px;
  height: 100px;
  background-color: rebeccapurple;
  transform: rotate(0.8turn)/*将方块旋转0.8周*/
}
```

`<background-image>`为一个内容设置一个或多个背景(通过函数控制显示)

`<color>`设置背景颜色（颜色可通过函数计算）

## @rule

### @import

```css
@import 'styles2.css'
```

- 将其它CSS表导入主表中

### @media

```css
body {
  background-color: pink;
}

@media (min-width: 30em) {
  body {
    background-color: blue;
  }
}
/*当窗口宽度大于30em时背景显示为蓝色，否则为粉色*/
```

## 速记属性

- 一些属性可以允许一行设置多个值，从而使代码更简洁，如`font`,`background`,`padding`,`border`,`margin`，例如

```css
padding: 10px 15px 15px 5px;
```

等价于这四行代码

```css
padding-top: 10px;
padding-right: 15px;
padding-bottom: 15px;
padding-left: 5px;
```

这一行：

```css
background: red url(bg-graphic.png) 10px 10px repeat-x fixed;
```

与这五行等价：

```css
background-color: red;
background-image: url(bg-graphic.png);
background-position: 10px 10px;
background-repeat: repeat-x;
background-attachment: fixed;
```

