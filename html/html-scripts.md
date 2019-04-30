# HTML 脚本

JavaScript 使 HTML 页面具有更强的动态和交互性。

## 在线实例

<a target="_blank" href="../run/run.html#filename=html_script">插入一段脚本</a>

如何将脚本插入 html 文档。

<a target="_blank" href="../run/run.html#filename=html_noscript">使用 `<noscript>`  标签</a>

如何应对不支持脚本或禁用脚本的浏览器。

## HTML &lt;script&gt; 标签

`<script>` 标签用于定义客户端脚本，比如 JavaScript。

`<script>` 元素既可包含脚本语句，也可通过 src 属性指向外部脚本文件。

JavaScript 最常用于图片操作、表单验证以及内容动态更新。

下面的脚本会向浏览器输出"Hello World!"：

<!--sec data-title="实例" data-filename="html_script" ces-->
```html
<script> document.write("Hello World!"); </script>
```
<!--endsec-->

学习更多关于Javascript教程，请查看 [JavaScript 教程](../js/js-tutorial.md "JavaScript 教程")!

## HTML&lt;noscript&gt; 标签

`<noscript>` 标签提供无法使用脚本时的替代内容，比方在浏览器禁用脚本时，或浏览器不支持客户端脚本时。

`<noscript>`元素可包含普通 HTML 页面的 body 元素中能够找到的所有元素。

只有在浏览器不支持脚本或者禁用脚本时，才会显示 <noscript>  元素中的内容：

<!--sec data-title="实例" data-filename="html_noscript" ces-->
```html
<script>
document.write("Hello World!")
</script>
<noscript>抱歉，你的浏览器不支持 JavaScript!</noscript>
```
<!--endsec-->

## JavaScript体验(来自本站javascript教程)

JavaScript实例代码:

<!--sec data-title="JavaScript可以直接在HTML输出" data-filename="js_intro_document_write" ces-->
```javascript
document.write("<p>这是一个段落。</p>");
```
<!--endsec-->

<!--sec data-title="JavaScript事件响应" data-filename="js_intro_event" ces-->
```html
<button type ="button" onclick ="myFunction()"> 点我！ </button>
```
<!--endsec-->

<!--sec data-title="JavaScript处理 HTML 样式" data-filename="js_intro_style" ces-->
```javascript
document.getElementById("demo").style.color = "#ff0000";
```
<!--endsec-->

## HTML 脚本标签

| 标签 | 描述 |
| :------------  | :------------ |
| [`<script>`](../tags/tag-script.md "<script>") | 定义了客户端脚本 |
| [`<noscript>`](../tags/tag-noscript.md "<noscript>") | 定义了不支持脚本浏览器输出的文本 |
