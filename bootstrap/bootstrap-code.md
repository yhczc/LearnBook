# Bootstrap 代码

Bootstrap 允许您以两种方式显示代码：

- 第一种是 `<code>` 标签。如果您想要内联显示代码，那么您应该使用 `<code>` 标签。
- 第二种是 `<pre>` 标签。如果代码需要被显示为一个独立的块元素或者代码有多行，那么您应该使用 `<pre>` 标签。

请确保当您使用 `<pre>` 和 `<code>` 标签时，开始和结束标签使用了 unicode 变体：** &amp;lt;** 和 **&amp;gt;**。

让我们来看看下面的实例：

<!--sec data-title="实例" data-filename="bootstrap3-code" ces-->
```html
<p><code>&lt;header&gt;</code> 作为内联元素被包围。</p>
<p>如果需要把代码显示为一个独立的块元素，请使用 &lt;pre&gt; 标签：</p>
<pre>
    &lt;article&gt;
        &lt;h1&gt;Article Heading&lt;/h1&gt;
    &lt;/article&gt;
</pre>
```
<!--endsec-->

实例展示如下图：

![代码](img/code_demo.jpg "代码")

## 更多实例

| 元素/类 | 描述 | 实例 |
| :------------  | :------------ | :------------ |
| `<var>` | 变量赋值: x = ab + y | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_var "实例") |
| `<kbd>` | 按键提示： CTRL + P | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_kbd "实例") |
| `<pre>` | 多行代码 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_pre "实例") |
| `<pre class="pre-scrollable">` | 多行代码带有滚动条 | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_pre "实例") |
| `<samp>` | 电脑程序输出: Sample output | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_samp "实例") |
| `<code>` | 同一行代码片段: span, div | [实例](http://www.gitmt.com/run/run.html#filename=bs_ref_txt_code "实例") |