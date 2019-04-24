# JavaScript HTML DOM - 改变 HTML

HTML DOM 允许 JavaScript 改变 HTML 元素的内容。

## 改变 HTML 输出流

JavaScript 能够创建动态的 HTML 内容：

**今天的日期是： <script>document.write(Date());</script>**

在 JavaScript 中，document.write() 可用于直接向 HTML 输出流写内容。

<!--sec data-title="实例" data-filename="dhtml_date" ces-->
```html
<!DOCTYPE html>
<html>
<body>

<script>
document.write(Date());
</script>

</body>
</html>
```
<!--endsec-->

> [!TIP]
> 绝对不要在文档(DOM)加载完成之后使用 document.write()。这会覆盖该文档。

## 改变 HTML 内容

修改 HTML 内容的最简单的方法是使用 innerHTML 属性。

如需改变 HTML 元素的内容，请使用这个语法：

```
document.getElementById(id).innerHTML=新的 HTML
```

本例改变了 `<p>`元素的内容：

<!--sec data-title="实例" data-filename="js_change_innerhtml" ces-->
```html
<html>
<body>

<p id="p1">Hello World!</p>

<script>
document.getElementById("p1").innerHTML="新文本!";
</script>

</body>
</html>
```
<!--endsec-->

本例改变了 `<h1>` 元素的内容：

<!--sec data-title="实例" data-filename="dhtml_dom_innertext" ces-->
```html
<!DOCTYPE html>
<html>
<body>

<h1 id="header">Old Header</h1>

<script>
var element=document.getElementById("header");
element.innerHTML="新标题";
</script>

</body>
</html>
```
<!--endsec-->

实例讲解：

- 上面的 HTML 文档含有 id="header" 的 `<h1>` 元素

- 我们使用 HTML DOM 来获得 id="header" 的元素

- JavaScript 更改此元素的内容 (innerHTML)

## 改变 HTML 属性

如需改变 HTML 元素的属性，请使用这个语法：

```
document.getElementById(id).attribute=新属性值
```

本例改变了 `<img>` 元素的 src 属性：

<!--sec data-title="实例" data-filename="dhtml_dom_image" ces-->
```html
<!DOCTYPE html>
<html>
<body>

<img id="image" src="smiley.gif">

<script>
document.getElementById("image").src="landscape.jpg";
</script>

</body>
</html>
```
<!--endsec-->

实例讲解：

- 上面的 HTML 文档含有 id="image" 的 `<img>` 元素
- 我们使用 HTML DOM 来获得 id="image" 的元素
- JavaScript 更改此元素的属性（把 "smiley.gif" 改为 "landscape.jpg"）

