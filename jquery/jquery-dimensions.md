# jQuery 尺寸

通过 jQuery，很容易处理元素和浏览器窗口的尺寸。

## jQuery 尺寸方法

jQuery 提供多个处理尺寸的重要方法：

- width()
- height()
- innerWidth()
- innerHeight()
- outerWidth()
- outerHeight()

## jQuery 尺寸

![jQuery Dimensions](img_jquerydim.gif "a")

## jQuery width() 和 height() 方法

width() 方法设置或返回元素的宽度（不包括内边距、边框或外边距）。

height() 方法设置或返回元素的高度（不包括内边距、边框或外边距）。

下面的例子返回指定的 `<div>` 元素的宽度和高度：

<!--sec data-title="实例" data-filename="jquery_dim_width_height" ces-->
```javascript
$("button").click(function(){
    var txt="";
    txt+="div 的宽度是: " + $("#div1").width() + "</br>";
    txt+="div 的高度是: " + $("#div1").height();
  $("#div1").html(txt);
});
```
<!--endsec-->

## jQuery innerWidth() 和 innerHeight() 方法

innerWidth() 方法返回元素的宽度（包括内边距）。

innerHeight() 方法返回元素的高度（包括内边距）。

下面的例子返回指定的 `<div>` 元素的 inner-width/height：

<!--sec data-title="实例" data-filename="jquery_dim_innerwidth_height" ces-->
```javascript
$("button").click(function(){
    var txt="";
    txt+="div 宽度，包含内边距: " + $("#div1").innerWidth() + "</br>";
    txt+="div 高度，包含内边距: " + $("#div1").innerHeight();
    $("#div1").html(txt);
});
```
<!--endsec-->

## jQuery outerWidth() 和 outerHeight() 方法

outerWidth() 方法返回元素的宽度（包括内边距和边框）。

outerHeight() 方法返回元素的高度（包括内边距和边框）。

下面的例子返回指定的 `<div>` 元素的 outer-width/height：

<!--sec data-title="实例" data-filename="jquery_dim_outerwidth_height" ces-->
```javascript
$("button").click(function(){
    var txt="";
    txt+="div 宽度，包含内边距和边框: " + $("#div1").outerWidth() + "</br>";
    txt+="div 高度，包含内边距和边框: " + $("#div1").outerHeight();
    $("#div1").html(txt);
});
```
<!--endsec-->

