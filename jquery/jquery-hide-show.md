# jQuery 效果- 隐藏和显示

隐藏、显示、切换，滑动，淡入淡出，以及动画，哇哦！

## 实例

<a target="_blank" href="http://www.gitmt.com/run/run.html#filename=jquery_hide">jquery hide()</a>

简单的jquery hide()方法演示。

<a target="_blank" href="http://www.gitmt.com/run/run.html#filename=jquery_hide_explanations">jquery hide()</a>

另一个hide()实例。演示如何隐藏文本。

## jQuery hide() 和 show()

通过 jQuery，您可以使用 hide() 和 show() 方法来隐藏和显示 HTML 元素：

<!--sec data-title="实例" data-filename="jquery_hide_show" ces-->
```javascript
$("#hide").click(function(){
  $("p").hide();
});

$("#show").click(function(){
  $("p").show();
});
```
<!--endsec-->

**语法:**

```
$(selector).hide(speed,callback);
$(selector).show(speed,callback);
```

可选的 speed 参数规定隐藏/显示的速度，可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是隐藏或显示完成后所执行的函数名称。

下面的例子演示了带有 speed 参数的 hide() 方法：

<!--sec data-title="实例" data-filename="jquery_hide_slow" ces-->
```javascript
$("button").click(function(){
  $("p").hide(1000);
});
```
<!--endsec-->

下面的例子演示了带有 speed 参数的 hide() 方法，并使用回调函数：

<!--sec data-title="实例" data-filename="jquery_hide_slow2" ces-->
```javascript
$(document).ready(function(){
  $(".hidebtn").click(function(){
    $("div").hide(1000,"linear",function(){alert("Hide() 方法已完成!");
    });
  });
});
```
<!--endsec-->

第二个参数是一个字符串，表示过渡使用哪种缓动函数。（译者注：jQuery自身提供"linear" 和 "swing"，其他可以使用相关的插件）。

## jQuery toggle()

通过 jQuery，您可以使用 toggle() 方法来切换 hide() 和 show() 方法。

显示被隐藏的元素，并隐藏已显示的元素：

<!--sec data-title="实例" data-filename="jquery_toggle" ces-->
```javascript
$("button").click(function(){
  $("p").toggle();
});
```
<!--endsec-->

**语法:**

```
$(selector).toggle(speed,callback);
```

可选的 speed 参数规定隐藏/显示的速度，可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是隐藏或显示完成后所执行的函数名称。