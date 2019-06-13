# jQuery 遍历 - 祖先

祖先是父、祖父或曾祖父等等。


通过 jQuery，您能够向上遍历 DOM 树，以查找元素的祖先。

## 向上遍历 DOM 树

这些 jQuery 方法很有用，它们用于向上遍历 DOM 树：

- parent()
- parents()
- parentsUntil()

## jQuery parent() 方法

parent() 方法返回被选元素的直接父元素。

该方法只会向上一级对 DOM 树进行遍历。

下面的例子返回每个 `<span>` 元素的的直接父元素：

<!--sec data-title="实例" data-filename="jquery_parent" ces-->
```javascript
$(document).ready(function(){
  $("span").parent();
});
```
<!--endsec-->

## jQuery parents() 方法

parents() 方法返回被选元素的所有祖先元素，它一路向上直到文档的根元素 (`<html>`)。

下面的例子返回所有 `<span>` 元素的所有祖先：

<!--sec data-title="实例" data-filename="jquery_parents" ces-->
```javascript
$(document).ready(function(){
  $("span").parents();
});
```
<!--endsec-->

您也可以使用可选参数来过滤对祖先元素的搜索。

下面的例子返回所有 `<span>` 元素的所有祖先，并且它是 `<ul>` 元素：

<!--sec data-title="实例" data-filename="jquery_parents2" ces-->
```javascript
$(document).ready(function(){
  $("span").parents("ul");
});
```
<!--endsec-->

## jQuery parentsUntil() 方法

parentsUntil() 方法返回介于两个给定元素之间的所有祖先元素。

下面的例子返回介于 `<span>` 与 `<div>` 元素之间的所有祖先元素：

<!--sec data-title="实例" data-filename="jquery_parentsuntil" ces-->
```javascript
$(document).ready(function(){
  $("span").parentsUntil("div");
});
```
<!--endsec-->