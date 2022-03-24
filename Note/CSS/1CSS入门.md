# CSS入门

## CSS简介

- 为什么要用CSS
  - ~~当然是因为HTML渲染出来的页面太丑了~~
- CSS可以干嘛？
  - 改变标题和链接的颜色及大小
  - 可以用于创建布局
  - 甚至可以做一些特效

## CSS基本语法

- CSS是一门基于规则的语言

```css
h1{/*指明元素<h1>*/
    color: red;/*设置为红色*/
    font-size: 5em;/*字号设置为5em*/
}
```

- 语法由一个选择器(Selector)起头，它选择我们要添加样式的元素（此例中为1级标题`<h1>`）
  - 选择器可以有多个，用`,`隔开，例如`p,h1{..`
- 接着是一个大括号，大括号内有多个声明
- 声明的格式为：`属性(properties):值(value)`

## 使用类

- 在大多数时候，我们不需要将所有同类元素设为一样的格式，此时用类进行区分

- 用法：

  - 先在html的元素中加入`class`属性

  ```html
  <p class="special"></p>
  ```

  - 在CSS里选中`.类名`设置格式

  ```css
  .special{
      color: blue;
  }
  ```

  - 也可以通过`元素名.类名`，设置该类下特定元素的格式

  ```css
  p.special{
      color: blue;
  }
  ```

## 根据位置设置格式

- 包含选择符：选择元素A内的元素B

```css
li em{/*选择<li>内的<em>*/
    ...
}
```

- 相邻选择符：选择元素A和元素A相邻的子元素B设置格式

```css
h1 + p {/*选择标题<h1>和第一段<p1>*/
    
}
```

## 根据状态设置格式

- 选择器格式：`元素:状态`
- 例如：设置链接点击前为粉色，访问后为绿色

```css
a:link{
    color: pink;
}

a: visited{
    color: green;
}
```

## 复杂选择器

- 可以组合上述的格式形成更复杂的选择器

一些栗子~

```css
/* selects any <span> that is inside a <p>, which is inside an <article>  */
article p span { ... }

/* selects any <p> that comes directly after a <ul>, which comes directly after an <h1>  */
h1 + ul + p { ... }

/* selects any p in class special that is directly after <h1>, which is inside a <*/
body h1 + p .special { ... }
```

