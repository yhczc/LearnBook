# jQuery - 设置内容和属性

## 设置内容 - text()、html() 以及 val()

我们将使用前一章中的三个相同的方法来设置内容：

- text() - 设置或返回所选元素的文本内容
- html() - 设置或返回所选元素的内容（包括 HTML 标记）
- val() - 设置或返回表单字段的值

下面的例子演示如何通过 text()、html() 以及 val() 方法来设置内容：

<!--sec data-title="实例" data-filename="jquery_dom_html_set" ces-->
```javascript
$("#btn1").click(function(){
    $("#test1").text("Hello world!");
});
$("#btn2").click(function(){
    $("#test2").html("<b>Hello world!</b>");
});
$("#btn3").click(function(){
    $("#test3").val("RUNOOB");
});
```
<!--endsec-->

## text()、html() 以及 val() 的回调函数

上面的三个 jQuery 方法：text()、html() 以及 val()，同样拥有回调函数。回调函数有两个参数：被选元素列表中当前元素的下标，以及原始（旧的）值。然后以函数新值返回您希望使用的字符串。

下面的例子演示带有回调函数的 text() 和 html()：

<!--sec data-title="实例" data-filename="jquery_dom_html_callback" ces-->
```javascript
$("#btn1").click(function(){
    $("#test1").text(function(i,origText){
        return"旧文本: " + origText + " 新文本: Hello world! (index: " + i + ")";
    });
});

$("#btn2").click(function(){
    $("#test2").html(function(i,origText){
        return"旧 html: " + origText + " 新 html: Hello <b>world!</b> (index: " + i + ")";
    });
});
```
<!--endsec-->

## 设置属性 - attr()

jQuery attr() 方法也用于设置/改变属性值。

下面的例子演示如何改变（设置）链接中 href 属性的值：

<!--sec data-title="实例" data-filename="jquery_dom_attr_set" ces-->
```javascript
$("button").click(function(){
  $("#gitmt").attr("href","http://www.gitmt.com/jquery");
});
```
<!--endsec-->

attr() 方法也允许您同时设置多个属性。

下面的例子演示如何同时设置 href 和 title 属性：

<!--sec data-title="实例" data-filename="jquery_dom_attr_set2" ces-->
```javascript
$("button").click(function(){
    $("#gitmt").attr({
        "href" : "http://www.gitmt.com/jquery",
        "title" : "jQuery 教程"
    });
});
```
<!--endsec-->

## attr() 的回调函数

jQuery 方法 attr()，也提供回调函数。回调函数有两个参数：被选元素列表中当前元素的下标，以及原始（旧的）值。然后以函数新值返回您希望使用的字符串。

下面的例子演示带有回调函数的 attr() 方法：

<!--sec data-title="实例" data-filename="jquery_dom_attr_callback" ces-->
```javascript
$("button").click(function(){
  $("#gitmt").attr("href", function(i,origValue){
      return origValue + "/jquery";
  });
});
```
<!--endsec-->