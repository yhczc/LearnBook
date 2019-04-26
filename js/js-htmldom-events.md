<script type = "text/javascript">
function clickMeEvent(obj) {
    if (obj.innerHTML == "Goodbye") {
        obj.style.display = "none";
    } else if (obj.innerHTML == "Thank You") {
        obj.innerHTML = "Goodbye";
    } else if (obj.innerHTML == "Click Me<br>Click Me Again<br>And Again") {
        obj.innerHTML = "Thank You";
    } else if (obj.innerHTML == "Click Me<br>Click Me Again") {
        obj.innerHTML = obj.innerHTML + "<br>And Again";
    } else {
        obj.innerHTML = obj.innerHTML + "<br>Click Me Again";
    }
} 
</script>
<script type = "text/javascript">
function mDown(obj) {
    obj.style.backgroundColor = "#1ec5e5";
    obj.innerHTML = "Release Me "
}
function mUp(obj) {
    obj.style.backgroundColor = "#D94A38";
    obj.innerHTML = "Thank You "
} </script>

# JavaScript HTML DOM 事件

HTML DOM 使 JavaScript 有能力对 HTML 事件做出反应。

<!--sec data-title="实例" data-filename="" ces-->
  <div style="width:100%;height:140px;"> 
   <div style="background-color:#D94A38;width:170px;height:80px;margin:20px;padding-top:20px;color:#ffffff;font-weight:bold;font-size:18px;float:left;text-align:center;" onmouseover="this.innerHTML='Thank You'" onmouseout="this.innerHTML='Mouse Over Me'">
     Mouse Over Me 
   </div> 
   <div style="background-color:#D94A38;width:170px;height:80px;margin:20px;padding-top:20px;color:#ffffff;font-weight:bold;font-size:18px;float:left;text-align:center;" onclick="clickMeEvent(this)">
     Click Me 
   </div> 
  </div>
<!--endsec-->

## 对事件做出反应

我们可以在事件发生时执行 JavaScript，比如当用户在 HTML 元素上点击时。

如需在用户点击某个元素时执行代码，请向一个 HTML 事件属性添加 JavaScript 代码：

```
onclick=JavaScript
```

HTML 事件的例子：

- 当用户点击鼠标时
- 当网页已加载时
- 当图像已加载时
- 当鼠标移动到元素上时
- 当输入字段被改变时
- 当提交 HTML 表单时
- 当用户触发按键时

在本例中，当用户在  `<h1>` 元素上点击时，会改变其内容：

<!--sec data-title="实例" data-filename="dhtml_event_onclick2" ces-->
```html
<!DOCTYPE html>
<html>
<body>
<h1 onclick="this.innerHTML='Ooops!'">点击文本!</h1>
</body>
</html>
```
<!--endsec-->

本例从事件处理器调用一个函数：

<!--sec data-title="实例" data-filename="dhtml_event_onclick3" ces-->
```html
<!DOCTYPE html>
<html>
<head>
<script>
function changetext(id)
{
    id.innerHTML="Ooops!";
}
</script>
</head>
<body>
<h1 onclick="changetext(this)">点击文本!</h1>
</body>
</html>
```
<!--endsec-->

## HTML 事件属性

如需向 HTML 元素分配 事件，您可以使用事件属性。

<!--sec data-title="实例" data-filename="js_events1" ces-->
向 button 元素分配 onclick 事件：

```html
<button onclick="displayDate()">点这里</button>
```
<!--endsec-->

在上面的例子中，名为 displayDate 的函数将在按钮被点击时执行。

## 使用 HTML DOM 来分配事件

HTML DOM 允许您使用 JavaScript 来向 HTML 元素分配事件：

<!--sec data-title="实例" data-filename="js_events2" ces-->
向 button 元素分配 onclick 事件：

```html
<script>
document.getElementById("myBtn").onclick=function() {displayDate()};
</script>
```
<!--endsec-->

在上面的例子中，名为 displayDate 的函数被分配给 id="myBtn" 的 HTML 元素。

按钮点击时Javascript函数将会被执行。

## onload 和 onunload 事件

onload 和 onunload 事件会在用户进入或离开页面时被触发。

onload 事件可用于检测访问者的浏览器类型和浏览器版本，并基于这些信息来加载网页的正确版本。

onload 和 onunload 事件可用于处理 cookie。

<!--sec data-title="实例" data-filename="js_events_onload" ces-->
```html
<body onload="checkCookies()">
```
<!--endsec-->

## onchange 事件

onchange 事件常结合对输入字段的验证来使用。

下面是一个如何使用 onchange 的例子。当用户改变输入字段的内容时，会调用 upperCase() 函数。

<!--sec data-title="实例" data-filename="jsref_onchange" ces-->
```html
<input type="text" id="fname" onchange="upperCase()">
```
<!--endsec-->

## onmouseover 和 onmouseout 事件

onmouseover 和 onmouseout 事件可用于在用户的鼠标移至 HTML 元素上方或移出元素时触发函数。

<!--sec data-title="实例" data-filename="js_events_mouseover" ces-->
一个简单的 onmouseover-onmouseout 实例：

<div style="width:100%;height:140px;"> 
   <div style="background-color:#D94A38;width:170px;height:80px;margin:20px;padding-top:20px;color:#ffffff;font-weight:bold;font-size:18px;float:left;text-align:center;" onmouseover="this.innerHTML='Thank You'" onmouseout="this.innerHTML='Mouse Over Me'">
    Mouse Over Me
   </div> 
  </div>
<!--endsec-->

## onmousedown、onmouseup 以及 onclick 事件

onmousedown, onmouseup 以及 onclick 构成了鼠标点击事件的所有部分。首先当点击鼠标按钮时，会触发 onmousedown 事件，当释放鼠标按钮时，会触发 onmouseup 事件，最后，当完成鼠标点击时，会触发 onclick 事件。

<!--sec data-title="实例" data-filename="" ces-->
一个简单的 onmousedown-onmouseup 实例：

<div style="width:100%;height:140px;"> 
   <div onmousedown="mDown(this)" onmouseup="mUp(this)" style="background-color: rgb(217, 74, 56); width: 170px; height: 80px; margin: 20px; padding-top: 20px; color: rgb(255, 255, 255); font-weight: bold; font-size: 18px; float: left; text-align: center;">
    Thank You
   </div> 
</div>
<!--endsec-->

## 更多实例

<a target="_blank" href="/run/run.html#filename=dhtml_event_onmousedown">onmousedown 和onmouseup</a>

当用户按下鼠标按钮时，更换一幅图像。

<a target="_blank" href="/run/run.html#filename=dhtml_event_onload">onload</a>

当页面完成加载时，显示一个提示框。

<a target="_blank" href="/run/run.html#filename=jsref_onfocus">onfocus</a>

当输入字段获得焦点时，改变其背景色。

<a target="_blank" href="/run/run.html#filename=dhtml_event_onmouse">鼠标事件</a>

当指针移动到元素上方时，改变其颜色；当指针移出文本后，会再次改变其颜色。