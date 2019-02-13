# HTML 样式
style 属性用于改变 HTML 元素的样式。
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="VgbNeG" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 样式">
  <span>See the Pen <a href="https://codepen.io/yhczc/pen/VgbNeG/">
  HTML 样式</a> by yhczc (<a href="https://codepen.io/yhczc">@yhczc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
## HTML 的 style 属性
style 属性的作用：
**提供了一种改变所有 HTML 元素的样式的通用方法。**
样式是 HTML 4 引入的，它是一种新的首选的改变 HTML 元素样式的方式。通过 HTML 样式，能够通过使用 style 属性直接将样式添加到 HTML 元素，或者间接地在独立的样式表中（CSS 文件）进行定义。
您可以在我们的[ CSS 教程](http://## " CSS 教程")中学习关于样式和 CSS 的所有知识。
在我们的 HTML 教程中，我们将使用 style 属性向您讲解 HTML 样式。
## 不赞成使用的标签和属性
在 HTML 4 中，有若干的标签和属性是被废弃的。被废弃（Deprecated）的意思是在未来版本的 HTML 和 XHTML 中将不支持这些标签和属性。
这里传达的信息很明确：请避免使用这些被废弃的标签和属性！
## 应该避免使用下面这些标签和属性：
| 标签  | 描述  |
| :------------ | :------------ |
| `<center>`  | 定义居中的内容。  |
| `<font>` 和 `<basefont>` | 定义 HTML 字体。 |
| `<s>`和 `<strike>` | 定义删除线文本  |
| `<u>` | 定义下划线文本  |

| 属性  | 描述  |
| :------------ | :------------ |
| align  | 定义文本的对齐方式  |
| bgcolor  | 定义背景颜色  |
| color  | 定义文本颜色  |

>**注意：**对于以上这些标签和属性：请使用样式代替！

## HTML 样式实例 - 背景颜色
background-color 属性为元素定义了背景颜色：
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="VgbNKE" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 样式实例 - 背景颜色">
style 属性淘汰了“旧的” bgcolor 属性。 
## HTML 样式实例 - 字体、颜色和尺寸
font-family、color 以及 font-size 属性分别定义元素中文本的字体系列、颜色和字体尺寸：
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="zewXoP" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 样式实例 - 字体、颜色和尺寸">
style 属性淘汰了旧的 <font> 标签。
## HTML 样式实例 - 文本对齐
text-align 属性规定了元素中文本的水平对齐方式：
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="Nojmax" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 样式实例 - 文本对齐">
style 属性淘汰了旧的 "align" 属性。



