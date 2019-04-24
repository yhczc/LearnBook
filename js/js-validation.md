# JavaScript 表单

## JavaScript 表单验证

HTML 表单验证可以通过 JavaScript 来完成。

以下实例代码用于判断表单字段(fname)值是否存在，如果存在，则弹出信息，否则阻止表单提交：

```javascript
function validateForm() {
    var x = document.forms["myForm"]["fname"].value;
    if (x == null || x == "") {
        alert("需要输入名字。");
        return false;
    }
}
```
以上 JavaScript 代码可以通过 HTML 代码来调用：

<!--sec data-title="HTML 表单实例" data-filename="js_validation_js" ces-->
```html
<form name="myForm" action="demo_form.php" onsubmit="return validateForm()" method="post">
名字: <input type="text" name="fname">
<input type="submit" value="提交">
</form>
```
<!--endsec-->

## JavaScript 验证输入的数字

JavaScript 常用于对输入数字的验证：

<!--sec data-title="实例" data-filename="js_validation_number" ces-->
<script>
function myFunction() {
    var x;
    var text = "输入正确";

    //Get the value of input field with id="numb"
    x = document.getElementById("numb").value;

    // If x is Not a Number, or x is less than one, or x is grather than 10 then
    if (isNaN(x) || x < 1 || x > 10) {
        text = "输入错误";
    }
    document.getElementById("demo").innerHTML = text;
}
</script>

<p>请输入 1 到 10 之间的数字：</p>
<input id="numb" type="text">
<button type="button" onclick="myFunction()">提交</button>
<p id="demo"></p>
<!--endsec-->

## HTML 表单自动验证

HTML 表单验证也可以通过浏览器来自动完成。

如果表单字段 (fname) 的值为空,  **required** 属性会阻止表单提交：

<!--sec data-title="实例" data-filename="js_validation_html" ces-->
```html
<form action="demo_form.php" method="post">
  <input type="text" name="fname" required="required">
  <input type="submit" value="提交">
</form>
```
<!--endsec-->

> [!INFO]
> Internet Explorer 9 及更早 IE 浏览器不支持表单自动验证。

## 数据验证

数据验证用于确保用户输入的数据是有效的。

典型的数据验证有：

- 必需字段是否有输入?
- 用户是否输入了合法的数据?
- 在数字字段是否输入了文本?

大多数情况下，数据验证用于确保用户正确输入数据。

数据验证可以使用不同方法来定义，并通过多种方式来调用。

**服务端数据验证**是在数据提交到服务器上后再验证。

**客户端数据验证 side validation**是在数据发送到服务器前，在浏览器上完成验证。

## HTML 约束验证

HTML5 新增了 HTML 表单的验证方式：约束验证（constraint validation）。

约束验证是表单被提交时浏览器用来实现验证的一种算法。

HTML 约束验证基于：

- HTML 输入属性
- CSS 伪类选择器
- DOM 属性和方法

### 约束验证 HTML 输入属性

| 属性 | 描述 |
| :------------  | :------------ |
| disabled | 规定输入的元素不可用 |
| max | 规定输入元素的最大值 |
| min | 规定输入元素的最小值 |
| pattern | 规定输入元素值的模式 |
| required | 规定输入元素字段是必需的 |
| type  | 规定输入元素的类型 |

完整列表，请查看 [HTML输入属性](../html/html5-form-attributes.html "HTML输入属性")。

### 约束验证 CSS 伪类选择器

| 选择器 | 描述 |
| :------------  | :------------ |
| :disabled | 选取属性为 "disabled" 属性的 input 元素 |
| :invalid | 选取无效的 input 元素 |
| :optional | 选择没有"required"属性的 input 元素 |
| :required | 选择有"required"属性的 input 元素 |
| :valid | 选取有效值的 input 元素 |

完整列表，请查看 [CSS 伪类](../css/css-pseudo-classes.html "CSS 伪类")。