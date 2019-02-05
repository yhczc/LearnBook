# HTML 样式- CSS
CSS (Cascading Style Sheets) 用于渲染HTML元素标签的样式.
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="QYgqdq" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 样式- CSS">
  <span>See the Pen <a href="https://codepen.io/yhczc/pen/QYgqdq/">
  HTML 样式- CSS</a> by yhczc (<a href="https://codepen.io/yhczc">@yhczc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
## 如何使用CSS
CSS 是在 HTML 4 开始使用的,是为了更好的渲染HTML元素而引入的.
CSS 可以通过以下方式添加到HTML中:
- 内联样式- 在HTML元素中使用"style" **属性**
- 内部样式表 -在HTML文档头部 `<head>` 区域使用`<style>` **元素** 来包含CSS
- 外部引用 - 使用外部 CSS **文件**

最好的方式是通过外部引用CSS文件.
在本站的HTML教程中我们使用了内联CSS样式来介绍实例，这是为了简化的例子，也使得你能更容易在线编辑代码并在线运行实例。
你可以通过本站的CSS教程 [CSS 教程](http://index.html "CSS 教程")学习更多的CSS知识.
## 内联样式
当特殊的样式需要应用到个别元素时，就可以使用内联样式。 使用内联样式的方法是在相关的标签中使用样式属性。样式属性可以包含任何 CSS 属性。以下实例显示出如何改变段落的颜色和左外边距。
```html
<p style="color:blue;margin-left:20px;">This is a paragraph.</p>
```
## HTML样式实例 - 背景颜色
背景色属性（background-color）定义一个元素的背景颜色：
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="VgbNKE" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 样式实例 - 背景颜色">
  <span>See the Pen <a href="https://codepen.io/yhczc/pen/VgbNKE/">
  HTML 样式实例 - 背景颜色</a> by yhczc (<a href="https://codepen.io/yhczc">@yhczc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
  
 早期背景色属性（background-color）是使用 bgcolor 属性定义。
##  HTML 样式实例 - 字体, 字体颜色 ，字体大小
我们可以使用font-family（字体），color（颜色），和font-size（字体大小）属性来定义字体的样式:
 <p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="zewXoP" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 样式实例 - 字体、颜色和尺寸">
  <span>See the Pen <a href="https://codepen.io/yhczc/pen/zewXoP/">
  HTML 样式实例 - 字体、颜色和尺寸</a> by yhczc (<a href="https://codepen.io/yhczc">@yhczc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
  
现在通常使用font-family（字体），color（颜色），和font-size（字体大小）属性来定义文本样式，而不是使用`<font>`标签。
## HTML 样式实例 - 文本对齐方式
使用 text-align（文字对齐）属性指定文本的水平与垂直对齐方式：  
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="Nojmax" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 样式实例 - 文本对齐">
  <span>See the Pen <a href="https://codepen.io/yhczc/pen/Nojmax/">
  HTML 样式实例 - 文本对齐</a> by yhczc (<a href="https://codepen.io/yhczc">@yhczc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
  
文本对齐属性 text-align取代了旧标签 `<center>` 。
## 内部样式表
当单个文件需要特别样式时，就可以使用内部样式表。你可以在`<head>` 部分通过` <style>`标签定义内部样式表:
```html
<head>
<style type="text/css">
body {background-color:yellow;}
p {color:blue;}
</style>
</head>
```

## 外部样式表

当样式需要被应用到很多页面的时候，外部样式表将是理想的选择。使用外部样式表，你就可以通过更改一个文件来改变整个站点的外观。

```html
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```
## HTML 样式标签
| 标签  | 描述  |
| :------------ | :------------ |
| `<style>`  | 定义文本样式  |
| `<link>`  | 定义资源引用地址  |

## 已弃用的标签和属性
在HTML 4, 原来支持定义HTML元素样式的标签和属性已被弃用。这些标签将不支持新版本的HTML标签。
不建议使用的标签有: `<font>`, `<center>`, `<strike>`
不建议使用的属性: color 和 bgcolor.

 :triangular_flag_on_post:**<span style="font-size:20px; color:green;">经验</span>**


CSS修饰标签的样式，有 "内联" 和 "外引" 两种方式。
对于大部分标签，以上两种方法均可，且修改父级标签，子级标签特性也会改变。但某些标签确无法通过修改父级标签来改变子级标签特性，如a标签，修改其颜色特性，必须直接修改 a 标签的特性才可。
实例：
```html
<a href="#" style="color:red;" rel="nofollow">只能使用"内联"方式</a>
```

