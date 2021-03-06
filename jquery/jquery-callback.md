# jQuery Callback 方法

Callback 函数在当前动画 100% 完成之后执行。

## jQuery 动画的问题

许多 jQuery 函数涉及动画。这些函数也许会将 *speed* 或 *duration* 作为可选参数。

例子：*$("p").hide("slow")*

*speed* 或 *duration* 参数可以设置许多不同的值，比如 "slow", "fast", "normal" 或毫秒。

**实例**

以下实例在隐藏效果完全实现后回调函数:

<!--sec data-title="实例" data-filename="jquery_hide_callback" ces-->
```javascript
$("button").click(function(){
  $("p").hide("slow",function(){
    alert("段落现在被隐藏了");
  });
});
```
<!--endsec-->

以下实例没有回调函数，警告框会在隐藏效果完成前弹出：

<!--sec data-title="实例" data-filename="jquery_hide_no_callback" ces-->
```javascript
$("button").click(function(){
  $("p").hide(1000);
  alert("段落现在被隐藏了");
});
```
<!--endsec-->