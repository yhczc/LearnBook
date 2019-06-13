# jQuery 遍历 - 同胞(siblings)

同胞拥有相同的父元素。

通过 jQuery，您能够在 DOM 树中遍历元素的同胞元素。

## 在 DOM 树中水平遍历

有许多有用的方法让我们在 DOM 树进行水平遍历：

- siblings()
- next()
- nextAll()
- nextUntil()
- prev()
- prevAll()
- prevUntil()

## jQuery siblings() 方法

siblings() 方法返回被选元素的所有同胞元素。

下面的例子返回 `<h2>` 的所有同胞元素：

<!--sec data-title="实例" data-filename="jquery_siblings" ces-->
```javascript
$(document).ready(function(){
  $("h2").siblings();
});
```
<!--endsec-->

您也可以使用可选参数来过滤对同胞元素的搜索。

下面的例子返回属于 `<h2>` 的同胞元素的所有 `<p>` 元素：

<!--sec data-title="实例" data-filename="jquery_siblings2" ces-->
```javascript
$(document).ready(function(){
  $("h2").siblings("p");
});
```
<!--endsec-->

## jQuery next() 方法

next() 方法返回被选元素的下一个同胞元素。

该方法只返回一个元素。

下面的例子返回 `<h2>` 的下一个同胞元素：

<!--sec data-title="实例" data-filename="jquery_next" ces-->
```javascript
$(document).ready(function(){
  $("h2").next();
});
```
<!--endsec-->

## jQuery nextAll() 方法

nextAll() 方法返回被选元素的所有跟随的同胞元素。

下面的例子返回 `<h2>` 的所有跟随的同胞元素：

<!--sec data-title="实例" data-filename="jquery_nextall" ces-->
```javascript
$(document).ready(function(){
  $("h2").nextAll();
});
```
<!--endsec-->

## jQuery nextUntil() 方法

nextUntil() 方法返回介于两个给定参数之间的所有跟随的同胞元素。

下面的例子返回介于 `<h2>` 与 `<h6>` 元素之间的所有同胞元素：

<!--sec data-title="实例" data-filename="jquery_nextuntil" ces-->
```javascript
$(document).ready(function(){
  $("h2").nextUntil("h6");
});
```
<!--endsec-->

## jQuery prev(), prevAll() & prevUntil() 方法

prev(), prevAll() 以及 prevUntil() 方法的工作方式与上面的方法类似，只不过方向相反而已：它们返回的是前面的同胞元素（在 DOM 树中沿着同胞之前元素遍历，而不是之后元素遍历）。