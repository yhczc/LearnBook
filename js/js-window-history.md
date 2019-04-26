# JavaScript Window History

window.history 对象包含浏览器的历史。

## Window History

**window.history**对象在编写时可不使用 window 这个前缀。

为了保护用户隐私，对 JavaScript 访问该对象的方法做出了限制。

一些方法：

- history.back() - 与在浏览器点击后退按钮相同
- history.forward() - 与在浏览器中点击向前按钮相同

## Window History Back

history.back()  方法加载历史列表中的前一个 URL。

这与在浏览器中点击后退按钮是相同的：

在页面上创建后退按钮：

<!--sec data-title="在页面上创建后退按钮" data-filename="" ces-->
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<head>
<script>
    function goBack()
    {
        window.history.back()
    }
</script>
</head>
<body>

<input type="button" value="Back" onclick="goBack()">

</body>
</html>
```

以上代码输出为：

<div class="example_code">

<input type="button" value="返回上一页" onclick="goBack()">
<script>
function goBack()
 {
 window.history.back()
 }
</script>
</div>
<!--endsec-->

## Window History Forward

history forward()  方法加载历史列表中的下一个 URL。

这与在浏览器中点击前进按钮是相同的：

在页面上创建一个向前的按钮：

<!--sec data-title="在页面上创建一个向前的按钮" data-filename="" ces-->
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<script>
function goForward()
{
    window.history.forward()
}
</script>
</head>
<body>
 
<input type="button" value="Forward" onclick="goForward()">
 
</body>
</html>
```

以上代码输出为：

<div class="example_code">

<input type="button" value="跳到下一页" onclick="goForward()">
<script>
function goForward()
 {
 window.history.forward()
 }
</script>
</div>
<!--endsec-->