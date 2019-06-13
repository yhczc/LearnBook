# jQuery 效果 - 滑动

jQuery 滑动方法可使元素上下滑动。

## 实例

<a target="_blank" href="http://www.gitmt.com/run/run.html#filename=jquery_slide_down">jquery slidedown()</a>

演示 jquery slidedown() 方法。

<a target="_blank" href="http://www.gitmt.com/run/run.html#filename=jquery_slide_up">jquery slideup()</a>

演示 jquery slideup() 方法。

<a target="_blank" href="http://www.gitmt.com/run/run.html#filename=jquery_slide_toggle">jquery slidetoggle()</a>

演示 jquery slidetoggle() 方法。

## jQuery 滑动方法

通过 jQuery，您可以在元素上创建滑动效果。

jQuery 拥有以下滑动方法：

- slideDown()
- slideUp()
- slideToggle()

## jQuery slideDown() 方法

jQuery slideDown() 方法用于向下滑动元素。

**语法:**

```
$(selector).slideDown(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是滑动完成后所执行的函数名称。

下面的例子演示了 slideDown() 方法：

<!--sec data-title="实例" data-filename="jquery_slide_down" ces-->
```javascript
$("#flip").click(function(){
  $("#panel").slideDown();
});
```
<!--endsec-->

## jQuery slideUp() 方法

jQuery slideUp() 方法用于向上滑动元素。

**语法:**

```
$(selector).slideUp(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是滑动完成后所执行的函数名称。

下面的例子演示了 slideUp() 方法：

<!--sec data-title="实例" data-filename="jquery_slide_up" ces-->
```javascript
$("#flip").click(function(){
  $("#panel").slideUp();
});
```
<!--endsec-->

## jQuery slideToggle() 方法

jQuery slideToggle() 方法可以在 slideDown() 与 slideUp() 方法之间进行切换。

如果元素向下滑动，则 slideToggle() 可向上滑动它们。

如果元素向上滑动，则 slideToggle() 可向下滑动它们。

```
$(selector).slideToggle(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是滑动完成后所执行的函数名称。

下面的例子演示了 slideToggle() 方法：

<!--sec data-title="实例" data-filename="jquery_slide_toggle" ces-->
```javascript
$("#flip").click(function(){
  $("#panel").slideToggle();
});
```
<!--endsec-->