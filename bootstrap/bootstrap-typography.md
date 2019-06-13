# Bootstrap 排版

Bootstrap 使用 Helvetica Neue、 Helvetica、 Arial 和 sans-serif 作为其默认的字体栈。

使用 Bootstrap 的排版特性，您可以创建标题、段落、列表及其他内联元素。

## 标题

Bootstrap 中定义了所有的 HTML 标题（h1 到 h6）的样式。请看下面的实例：

<!--sec data-title="实例" data-filename="bootstrap3-typography-headings" ces-->
```html
<h1>我是标题1 h1</h1>
<h2>我是标题2 h2</h2>
<h3>我是标题3 h3</h3>
<h4>我是标题4 h4</h4>
<h5>我是标题5 h5</h5>
<h6>我是标题6 h6</h6>
```
<!--endsec-->

结果如下所示：

![标题](img/headings_demo.jpg "标题")

### 内联子标题

如果需要向任何标题添加一个内联子标题，只需要简单地在元素两旁添加 `<small>`，或者添加 **.small** class，这样子您就能得到一个字号更小的颜色更浅的文本，如下面实例所示：

<!--sec data-title="实例" data-filename="bootstrap3-typography-inline-subheadings" ces-->
```html
<h1>我是标题1 h1. <small>我是副标题1 h1</small></h1>
<h2>我是标题2 h2. <small>我是副标题2 h2</small></h2>
<h3>我是标题3 h3. <small>我是副标题3 h3</small></h3>
<h4>我是标题4 h4. <small>我是副标题4 h4</small></h4>
<h5>我是标题5 h5. <small>我是副标题5 h5</small></h5>
<h6>我是标题6 h6. <small>我是副标题6 h6</small></h6>
```
<!--endsec-->

结果如下所示：

![内联子标题](img/inline_subheadings_demo.jpg "内联子标题")

## 引导主体副本

为了给段落添加强调文本，则可以添加 class="lead"，这将得到更大更粗、行高更高的文本，如下面实例所示：

<!--sec data-title="实例" data-filename="bootstrap3-typography-lead-bodycopy" ces-->
```html
<h2>引导主体副本</h2>
<p class="lead">这是一个演示引导主体副本用法的实例。这是一个演示引导主体副本用法的实例。这是一个演示引导主体副本用法的实例。这是一个演示引导主体副本用法的实例。这是一个演示引导主体副本用法的实例。这是一个演示引导主体副本用法的实例。这是一个演示引导主体副本用法的实例。这是一个演示引导主体副本用法的实例。</p>
```
<!--endsec-->

结果如下所示：

![引导主体副本](img/lead_bodycopy_demo.jpg "引导主体副本")

## 强调

HTML 的默认强调标签 `<small>`（设置文本为父文本大小的 85%）、`<strong>`（设置文本为更粗的文本）、`<em>`（设置文本为斜体）。

Bootstrap 提供了一些用于强调文本的类，如下面实例所示：

<!--sec data-title="实例" data-filename="bootstrap3-typography-emphasis" ces-->
```html
<small>本行内容是在标签内</small><br>
<strong>本行内容是在标签内</strong><br>
<em>本行内容是在标签内，并呈现为斜体</em><br>
<p class="text-left">向左对齐文本</p>
<p class="text-center">居中对齐文本</p>
<p class="text-right">向右对齐文本</p>
<p class="text-muted">本行内容是减弱的</p>
<p class="text-primary">本行内容带有一个 primary class</p>
<p class="text-success">本行内容带有一个 success class</p>
<p class="text-info">本行内容带有一个 info class</p>
<p class="text-warning">本行内容带有一个 warning class</p>
<p class="text-danger">本行内容带有一个 danger class</p>
```
<!--endsec-->

结果如下所示：

![强调](img/A4C37313-68D7-49B0-81F8-0BC4D23BC5AC.png "强调")

## 缩写

HTML 元素提供了用于缩写的标记，比如 WWW 或 HTTP。Bootstrap 定义 `<abbr>` 元素的样式为显示在文本底部的一条虚线边框，当鼠标悬停在上面时会显示完整的文本（只要您为 `<abbr>` title 属性添加了文本）。为了得到一个更小字体的文本，请添加 .initialism 到 `<abbr>`。

<!--sec data-title="实例" data-filename="bootstrap3-typography-abbreviation" ces-->
```html
<abbr title="World Wide Web">WWW</abbr><br>
<abbr title="Real Simple Syndication" class="initialism">RSS</abbr>
```
<!--endsec-->

结果如下所示：

![缩写](img/abbreviation_demo.jpg "缩写")

## 地址（Address）

使用 `<address>` 标签，您可以在网页上显示联系信息。由于 `<address>` 默认为 `display:block;`，您需要使用 `<br>` 标签来为封闭的地址文本添加换行。

<!--sec data-title="实例" data-filename="bootstrap3-typography-address" ces-->
```html
<address>
  <strong>Some Company, Inc.</strong><br>
  007 street<br>
  Some City, State XXXXX<br>
  <abbr title="Phone">P:</abbr> (123) 456-7890
</address>
<address>
  <strong>Full Name</strong><br>
  <a href="mailto:#">mailto@somedomain.com</a>
</address>
```
<!--endsec-->

结果如下所示：

![地址](img/address_demo.jpg "地址")

## 引用（Blockquote）

您可以在任意的 HTML 文本旁使用默认的 `<blockquote>`。其他选项包括，添加一个 `<small>` 标签来标识引用的来源，使用 class *.pull-right* 向右对齐引用。下面的实例演示了这些特性：

<!--sec data-title="实例" data-filename="bootstrap3-typography-blockquote" ces-->
```html
<blockquote>
  <p>
  这是一个默认的引用实例。这是一个默认的引用实例。这是一个默认的引用实例。这是一个默认的引用实例。这是一个默认的引用实例。这是一个默认的引用实例。这是一个默认的引用实例。这是一个默认的引用实例。
  </p>
</blockquote>
<blockquote>
  这是一个带有源标题的引用。
  <small>Someone famous in <cite title="Source Title">Source Title</cite></small>
</blockquote>
<blockquote class="pull-right">
  这是一个向右对齐的引用。
  <small>Someone famous in <cite title="Source Title">Source Title</cite></small>
</blockquote>
```
<!--endsec-->

结果如下所示：

![引用](img/blockquote_demo.jpg "引用")

## 列表

Bootstrap 支持有序列表、无序列表和定义列表。

- 有序列表：有序列表是指以数字或其他有序字符开头的列表。
- 无序列表：无序列表是指没有特定顺序的列表，是以传统风格的着重号开头的列表。如果您不想显示这些着重号，您可以使用 class .list-unstyled 来移除样式。您也可以通过使用 class .list-inline 把所有的列表项放在同一行中。
- 定义列表：在这种类型的列表中，每个列表项可以包含 `<dt>` 和 `<dd>` 元素。`<dt>` 代表 定义术语，就像字典。接着，`<dd>` 是 `<dt>` 的描述。.dl-horizontal 可以让 `<dl>` 内的短语及其描述排在一行。开始是像 `<dl>` 的默认样式堆叠在一起，随着导航条逐渐展开而排列在一行。

下面的实例演示了这些类型的列表：

<!--sec data-title="实例" data-filename="bootstrap3-typography-list" ces-->
```html
<h4>有序列表</h4>
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ol>
<h4>无序列表</h4>
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>
<h4>未定义样式列表</h4>
<ul class="list-unstyled">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>
<h4>内联列表</h4>
<ul class="list-inline">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>
<h4>定义列表</h4>
<dl>
  <dt>Description 1</dt>
  <dd>Item 1</dd>
  <dt>Description 2</dt>
  <dd>Item 2</dd>
</dl>
<h4>水平的定义列表</h4>
<dl class="dl-horizontal">
  <dt>Description 1</dt>
  <dd>Item 1</dd>
  <dt>Description 2</dt>
  <dd>Item 2</dd>
</dl>
```
<!--endsec-->

结果如下所示：

![列表](img/list_demo.jpg "列表")

## 更多排版类

下表提供了 Bootstrap 更多排版类的实例：

| 类 | 描述 | 实例 |
| :------------  | :------------ | :------------ |
| .lead | 使段落突出显示 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_lead "实例") |
| .small | 设定小文本 (设置为父文本的 85% 大小) | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_small "实例") |
| .text-left | 设定文本左对齐 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_text-left "实例") |
| .text-center | 设定文本居中对齐 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_text-left "实例") |
| .text-right | 设定文本右对齐 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_text-left "实例") |
| .text-justify | 设定文本对齐,段落中超出屏幕部分文字自动换行 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_text-left "实例") |
| .text-nowrap | 段落中超出屏幕部分不换行 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_text-left "实例") |
| .text-lowercase | 设定文本小写 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_text-lowercase "实例") |
| .text-uppercase | 设定文本大写 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_text-lowercase "实例") |
| .text-capitalize | 设定单词首字母大写 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_text-lowercase "实例") |
| .initialism | 显示在 `<abbr>` 元素中的文本以小号字体展示，且可以将小写字母转换为大写字母 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_abbr2 "实例") |
| .blockquote-reverse | 设定引用右对齐 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_blockquote2 "实例") |
| .list-unstyled | 移除默认的列表样式，列表项中左对齐 ( `<ul>` 和 `<ol>` 中)。 这个类仅适用于直接子列表项 (如果需要移除嵌套的列表项，你需要在嵌套的列表中使用该样式) | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_list-unstyled "实例") |
| .list-inline | 将所有列表项放置同一行 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_list-inline "实例") |
| .dl-horizontal | 该类设置了浮动和偏移，应用于 `<dl>` 元素和 `<dt>` 元素中，具体实现可以查看实例 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_dl-horizontal "实例") |
| .pre-scrollable | 使 `<pre>` 元素可滚动，代码块区域最大高度为340px,一旦超出这个高度,就会在Y轴出现滚动条 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_pre2 "实例") |
