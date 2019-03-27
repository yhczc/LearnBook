### CSS 表格

HTML中，专门用来创建表格的标签多得吓人，而最常用的有 `<table>`、`<caption>`、`<thead>`、`<tbody>`、`<tr>`、`<th>`、`<td>` 这 7 个标签。

`<table>` 标签用于定义一个表格；`<caption>` 标签用于定义表格的大标题，习惯放在表格定义的第一行，即紧随 `<table>` 标签；`<tr>` 标签用来定义表格的行；`<th>` 标签用于定义行或列的名称，即表头，其中的内容默认会加粗居中显示；`<td>` 标签用于定义表格的单元格，来存放表格的数据。

为了方便控制样式，一般把表头放在 thead 元素中，表格正文放在 tbody 元素中。代码如下：


<!--sec data-title="实例" data-filename="css_table" ces-->
```html
<table>
<caption>HTML表格示例</caption>
       <thead>
 <tr>
          <th>表头1</th>
          <th>表头2</th>
       </tr>
       </thead>
       <tbody>
       <tr>
          <td>单元格1</td>
          <td>单元格2</td>
       </tr>
       <tr>
          <td>单元格1</td>
          <td>单元格2</td>
       </tr>
       </tbody>
</table>
```
<!--endsec-->

## 基本布局

在可视化模型中，一个表格既可以生成块级框（display:table），也可以生成行内级框（display:inline-table），默认生成块级框。

无论是块级框，还是行内级框，table元素都会生成一个主框，其中包含一个 table 框和一个 caption 框。如下图所示：

![表格的可视化模型](/run/example_source.png "表格的可视化模型")

上图中，灰色虚线框的区域为 table元素形成的主框，蓝色区域为 table 框，红色区域为 caption 框，它们是两个独立的框，有各自独立的盒属性，如 marging、border等。主框的外边距，由 table元素 margin 属性定义。
