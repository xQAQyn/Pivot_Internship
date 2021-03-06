# HTML文字处理基础

## 标题与段落

- 标题(Heading)通过`<h..>`标签实现，共有6级标签
- 段落(Paragraph)通过`<p>`标签实现

### 结构层次

- 通过标题与段落可以实现结构层次，例如

```html
<h1>三国演义</h1>

<p>罗贯中</p>

<h2>第一回 宴桃园豪杰三结义 斩黄巾英雄首立功</h2>

<p>话说天下大势，分久必合，合久必分。周末七国分争，并入于秦。及秦灭之后，楚、汉分争，又并入于汉……</p>

<h2>第二回 张翼德怒鞭督邮 何国舅谋诛宦竖</h2>

<p>且说董卓字仲颖，陇西临洮人也，官拜河东太守，自来骄傲。当日怠慢了玄德，张飞性发，便欲杀之……</p>

<h3>却说张飞</h3>

<p>却说张飞饮了数杯闷酒，乘马从馆驿前过，见五六十个老人，皆在门前痛哭。飞问其故，众老人答曰：“督邮逼勒县吏，欲害刘公；我等皆来苦告，不得放入，反遭把门人赶打！”……</p>
```

- 结构层次需要合理，tips：
  - 最好只使用一次`<h1>`作为顶级标题
  - 以正确的层次结构使用标题，如`<h2>`的标题不可作为`<h3>`标题的子标题
  - 在6个标题级别中，在每一页使用的层次尽量不超过3个。

## 列表

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

### 嵌套列表

- 列表之间可以进行嵌套：

```html
<ul>
    <li>后端</li>
    <li>前端</li>
    <ul>
        <li>HTML</li>
        <li>CSS</li>
    </ul>
</ul>
```

## 重点强调

- 强调(Emphasis)——斜体：`<em><\em>`
- 重点(Strong importance)——粗体：`<strong></strong>`
