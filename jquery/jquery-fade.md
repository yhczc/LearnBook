# jQuery 效果 - 淡入淡出

通过 jQuery，您可以实现元素的淡入淡出效果。

## 实例

<a target="_blank" href="http://www.gitmt.com/run/run.html#filename=jquery_fadein">jquery fadein()</a>

演示 jquery fadein() 方法。

<a target="_blank" href="http://www.gitmt.com/run/run.html#filename=jquery_fadeout">jquery fadeout()</a>

演示 jquery fadeout() 方法。

<a target="_blank" href="http://www.gitmt.com/run/run.html#filename=jquery_fadetoggle">jquery 
fadetoggle()</a>

演示 jquery fadetoggle() 方法。

<a target="_blank" href="http://www.gitmt.com/run/run.html#filename=jquery_fadeto">jquery fadeto()</a>

演示 jquery fadeto() 方法。

## jQuery Fading 方法

通过 jQuery，您可以实现元素的淡入淡出效果。

jQuery 拥有下面四种 fade 方法：

- fadeIn()
- fadeOut()
- fadeToggle()
- fadeTo()

## jQuery fadeIn() 方法

jQuery fadeIn() 用于淡入已隐藏的元素。

**语法:**

```
$(selector).fadeIn(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。.

可选的 callback 参数是 fading 完成后所执行的函数名称。

下面的例子演示了带有不同参数的 fadeIn() 方法：

<!--sec data-title="实例" data-filename="jquery_fadein" ces-->
```javascript
$("button").click(function(){
  $("#div1").fadeIn();
  $("#div2").fadeIn("slow");
  $("#div3").fadeIn(3000);
});
```
<!--endsec-->

## jQuery fadeOut() 方法

jQuery fadeOut() 方法用于淡出可见元素。

**语法:**

```
$(selector).fadeOut(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是 fading 完成后所执行的函数名称。

下面的例子演示了带有不同参数的 fadeOut() 方法：

<!--sec data-title="实例" data-filename="jquery_fadeout" ces-->
```javascript
$("button").click(function(){
  $("#div1").fadeOut();
  $("#div2").fadeOut("slow");
  $("#div3").fadeOut(3000);
});
```
<!--endsec-->

## jQuery fadeToggle() 方法

jQuery fadeToggle() 方法可以在 fadeIn() 与 fadeOut() 方法之间进行切换。

如果元素已淡出，则 fadeToggle() 会向元素添加淡入效果。

如果元素已淡入，则 fadeToggle() 会向元素添加淡出效果。

**语法:**

```
$(selector).fadeToggle(speed,callback);
```

可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

可选的 callback 参数是 fading 完成后所执行的函数名称。

下面的例子演示了带有不同参数的 fadeToggle() 方法：

<!--sec data-title="实例" data-filename="jquery_fadetoggle" ces-->
```javascript
$("button").click(function(){
  $("#div1").fadeToggle();
  $("#div2").fadeToggle("slow");
  $("#div3").fadeToggle(3000);
});
```
<!--endsec-->

## jQuery fadeTo() 方法

jQuery fadeTo() 方法允许渐变为给定的不透明度（值介于 0 与 1 之间）。

**语法:**

```javascript

$(selector).fadeTo(speed,opacity,callback);
```

必需的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。

fadeTo() 方法中必需的 opacity 参数将淡入淡出效果设置为给定的不透明度（值介于 0 与 1 之间）。

可选的 callback 参数是该函数完成后所执行的函数名称。

下面的例子演示了带有不同参数的 fadeTo() 方法：

<!--sec data-title="实例" data-filename="jquery_fadeto" ces-->
```javascript
$("button").click(function(){
  $("#div1").fadeTo("slow",0.15);
  $("#div2").fadeTo("slow",0.4);
  $("#div3").fadeTo("slow",0.7);
});
```
<!--endsec-->