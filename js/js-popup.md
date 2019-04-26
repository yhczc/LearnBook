# JavaScript 弹窗

可以在 JavaScript 中创建三种消息框：警告框、确认框、提示框。

## 警告框

警告框经常用于确保用户可以得到某些信息。

当警告框出现后，用户需要点击确定按钮才能继续进行操作。 

### 语法

```javascript
window.alert("sometext");
```

**window.alert()** 方法可以不带上window对象，直接使用**alert()**方法。

<!--sec data-title="实例" data-filename="js_alert" ces-->
```html
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction()
{
    alert("你好，我是一个警告框！");
}
</script>
</head>
<body>

<input type="button" onclick="myFunction()" value="显示警告框">

</body>
</html>
```
<!--endsec-->

## 确认框

确认框通常用于验证是否接受用户操作。

当确认卡弹出时，用户可以点击 "确认" 或者 "取消" 来确定用户操作。 

当你点击 "确认", 确认框返回 true， 如果点击 "取消", 确认框返回 false。

### 语法

```javascript
window.confirm("sometext");
```

**window.confirm()** 方法可以不带上window对象，直接使用**confirm()**方法。

<!--sec data-title="实例" data-filename="js_confirm" ces-->
```html
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction()
{
    alert("你好，我是一个警告框！");
}
</script>
</head>
<body>

<input type="button" onclick="myFunction()" value="显示警告框">

</body>
</html>
```
<!--endsec-->

## 提示框

提示框经常用于提示用户在进入页面前输入某个值。

当提示框出现后，用户需要输入某个值，然后点击确认或取消按钮才能继续操纵。

如果用户点击确认，那么返回值为输入的值。如果用户点击取消，那么返回值为 null。

### 语法

```javascript
window.prompt("sometext","defaultvalue");
```

**window.prompt()** 方法可以不带上window对象，直接使用**prompt()**方法。

<!--sec data-title="实例" data-filename="js_prompt" ces-->
```javascript
var person = prompt("请输入你的名字", "Harry Potter");
if (person != null &&person != "")
{
    x = "你好 " + person + "! 今天感觉如何?";
    document.getElementById("demo").innerHTML = x;
}
```
<!--endsec-->

## 换行

弹窗使用 反斜杠 + "n"(\n) 来设置换行。

<!--sec data-title="实例" data-filename="js_alert2" ces-->
```javascript
alert("Hello\nHow are you?");
```
<!--endsec-->
