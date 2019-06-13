# jQuery 停止动画

jQuery stop() 方法用于在动画或效果完成前对它们进行停止。

## 实例

<a target="_blank" href="http://www.gitmt.com/run/run.html#filename=jquery_stop_slide">jquery stop() 滑动</a><

演示 jquery stop() 方法。

<a target="_blank" href="http://www.gitmt.com/run/run.html#filename=jquery_stop_params">jquery 
stop() 动画(带参数)</a>

演示 jquery stop() 方法

## jQuery stop() 方法

jQuery stop() 方法用于停止动画或效果，在它们完成之前。

stop() 方法适用于所有 jQuery 效果函数，包括滑动、淡入淡出和自定义动画。

**语法:**

```
$(selector).stop(stopAll,goToEnd);
```

可选的 stopAll 参数规定是否应该清除动画队列。默认是 false，即仅停止活动的动画，允许任何排入队列的动画向后执行。

可选的 goToEnd 参数规定是否立即完成当前动画。默认是 false。

因此，默认地，stop() 会清除在被选元素上指定的当前动画。

下面的例子演示 stop() 方法，不带参数：

<!--sec data-title="实例" data-filename="jquery_stop_slide" ces-->
```javascript
$("#stop").click(function(){
  $("#panel").stop();
});
```
<!--endsec-->
