# jQuery - 获取内容和属性

jQuery 拥有可操作 HTML 元素和属性的强大方法。

## jQuery DOM 操作

jQuery 中非常重要的部分，就是操作 DOM 的能力。

jQuery 提供一系列与 DOM 相关的方法，这使访问和操作元素和属性变得很容易。

> [!TIP]
> **DOM = Document Object Model（文档对象模型）**
> DOM 定义访问 HTML 和 XML 文档的标准：
> "W3C 文档对象模型独立于平台和语言的界面，允许程序和脚本动态访问和更新文档的内容、结构以及样式。"

## 获得内容 - text()、html() 以及 val()

三个简单实用的用于 DOM 操作的 jQuery 方法：

- text() - 设置或返回所选元素的文本内容
- html() - 设置或返回所选元素的内容（包括 HTML 标记）
- val() - 设置或返回表单字段的值

下面的例子演示如何通过 jQuery text() 和 html() 方法来获得内容：

<!--sec data-title="实例" data-filename="jquery_dom_html_get" ces-->
```javascript
$("#btn1").click(function(){
    alert("Text: " + $("#test").text());
});
$("#btn2").click(function(){
    alert("HTML: " + $("#test").html());
});
```
<!--endsec-->

下面的例子演示如何通过 jQuery val() 方法获得输入字段的值：

<!--sec data-title="实例" data-filename="jquery_dom_val_get" ces-->
```javascript
$("#btn1").click(function(){
    alert("值为: " + $("#test").val());
});
```
<!--endsec-->

## 获取属性 - attr()

jQuery attr() 方法用于获取属性值。

下面的例子演示如何获得链接中 href 属性的值：

<!--sec data-title="实例" data-filename="jquery_dom_attr_get" ces-->
```javascript
$("button").click(function(){
    alert($("#runoob").attr("href"));
});
```
<!--endsec-->

下一章会讲解如何设置（改变）内容和属性值。