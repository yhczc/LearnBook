# HTML 列表
HTML 支持有序、无序和定义列表:
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="exEWYe" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML列表 ">
  <span>See the Pen <a href="https://codepen.io/yhczc/pen/exEWYe/">
  HTML列表 </a> by yhczc (<a href="https://codepen.io/yhczc">@yhczc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
## HTML无序列表
无序列表是一个项目的列表，此列项目使用粗体圆点（典型的小黑圆圈）进行标记。
无序列表使用`<ul>` 标签
```html
<ul>
<li>Coffee</li>
<li>Milk</li>
</ul>
```
浏览器显示如下：
- Coffee
- Milk

## HTML 有序列表
同样，有序列表也是一列项目，列表项目使用数字进行标记。 有序列表始于 `<ol>` 标签。每个列表项始于 `<li>` 标签。
列表项使用数字来标记。
```html
<ol>
<li>Coffee</li>
<li>Milk</li>
</ol>
```
浏览器显示如下：
1. Coffee
2. Milk

## HTML 自定义列表
自定义列表不仅仅是一列项目，而是项目及其注释的组合。
自定义列表以 `<dl>` 标签开始。每个自定义列表项以 `<dt>` 开始。每个自定义列表项的定义以 `<dd>` 开始。
```html
<dl>
<dt>Coffee</dt>
<dd>- black hot drink</dd>
<dt>Milk</dt>
<dd>- white cold drink</dd>
</dl>
```
浏览器显示如下：
<dl>
<dt>Coffee</dt>
<dd>- black hot drink</dd>
<dt>Milk</dt>
<dd>- white cold drink</dd>
</dl>

### 注意事项 - 有用提示
**提示:** 列表项内部可以使用段落、换行符、图片、链接以及其他列表等等。
## HTML 列表标签
| 标签  | 描述  |
| :------------ | :------------ |
| `<ol>`  | 定义有序列表  |
| `<ul>`  | 定义无序列表  |
| `<li>`  | 定义列表项  |
| `<dl>`  | 定义列表  |
| `<dt>`  | 自定义列表项目  |
| `<dd>`  | 定义自定列表项的描述  |


