# JavaScript HTML DOM 集合(Collection)

本章节介绍如何向文档中添加和移除元素(节点)。

## HTMLCollection 对象

getElementsByTagName() 方法返回 <a rel="noopener" target="_blank" href="../jsref/dom-htmlcollection.md">HTMLCollection</a> 对象。

 HTMLCollection 对象类似包含 HTML 元素的一个数组。

以下代码获取文档所有的 `<p>` 元素：

<!--sec data-title="实例" data-filename="js_dom_htmlcollection" ces-->
```javascript
varx = document.getElementsByTagName("p");
```

集合中的元素可以通过索引(以 0 为起始位置)来访问。

访问第二个 `<p>` 元素可以是以下代码:

```javascript
y = x[1];
```
<!--endsec-->

## HTMLCollection 对象 length 属性

HTMLCollection 对象的 length 属性定义了集合中元素的数量。

<!--sec data-title="实例" data-filename="js_dom_htmlcollection_length" ces-->
```javascript
var myCollection = document.getElementsByTagName("p");
document.getElementById("demo").innerHTML = myCollection.length;
```
<!--endsec-->

### 实例解析

获取 `<p>` 元素的集合：

```javascript
var myCollection = document.getElementsByTagName("p");
```

显示集合元素个数：

```javascript
document.getElementById("demo").innerHTML = myCollection.length;
```

集合 length 属性常用于遍历集合中的元素。

<!--sec data-title="实例" data-filename="js_dom_htmlcollection_loop" ces-->
修改所有 `<p>` 元素的背景颜色:

```javascript
var myCollection = document.getElementsByTagName("p");
var i;
for (i = 0; i < myCollection.length; i++) {
    myCollection[i].style.backgroundColor = "red";
}
```
<!--endsec-->

### 注意

**HTMLCollection 不是一个数组！**

HTMLCollection 看起来可能是一个数组，但其实不是。

你可以像数组一样，使用索引来获取元素。

HTMLCollection 无法使用数组的方法： valueOf(), pop(), push(), 或 join() 。