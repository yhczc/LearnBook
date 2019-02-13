# HTML 表格
表格由 `<table>` 标签来定义。每个表格均有若干行（由 `<tr>` 标签定义），每行被分割为若干单元格（由 `<td>` 标签定义）。字母 td 指表格数据（table data），即数据单元格的内容。数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。
### HTML 表格实例:
<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="yhczc" data-slug-hash="wNeEwZ" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid black; margin: 1em 0; padding: 1em;" data-pen-title="HTML 表格实例">
  <span>See the Pen <a href="https://codepen.io/yhczc/pen/wNeEwZ/">
  HTML 表格实例</a> by yhczc (<a href="https://codepen.io/yhczc">@yhczc</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
## HTML 表格和边框属性
如果不定义边框属性，表格将不显示边框。有时这很有用，但是大多数时候，我们希望显示边框。
使用边框属性`border="1"`来显示一个带有边框的表格：
```html
<table border="1">
    <tr>
        <td>Row 1, cell 1</td>
        <td>Row 1, cell 2</td>
    </tr>
</table>
```
## HTML 表格表头
```html
<table border="1">
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>row 1, cell 1</td>
        <td>row 1, cell 2</td>
    </tr>
    <tr>
        <td>row 2, cell 1</td>
        <td>row 2, cell 2</td>
    </tr>
</table>
```
在浏览器显示如下：

<table id="table" border="1" style="display: table;
    border-collapse: separate;
    border-spacing: 2px;
    border-color: grey;width:auto">
    <tr style="display: table-row;
    vertical-align: inherit;
    border-color: inherit;">
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>row 1, cell 1</td>
        <td>row 1, cell 2</td>
    </tr>
    <tr>
        <td>row 2, cell 1</td>
        <td>row 2, cell 2</td>
    </tr>
</table>

## HTML 表格标签
| 标签  | 描述  |
| :------------ | :------------ |
| `<table>`  | 定义表格  |
| `<th>`  | 定义表格的表头  |
| `<tr>`  | 定义表格的行  |
| `<td>`  | 定义表格单元  |
| `<caption>` | 定义表格标题  |
| `<colgroup>`  | 定义表格列的组  |
| `<col>`  | 定义用于表格列的属性  |
| `<thead>`  | 定义表格的页眉  |
| `<tbody>`  | 定义表格的主体  |
| `<tfoot>`  | 定义表格的页脚  |

