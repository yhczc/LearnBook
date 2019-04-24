# JavaScript HTML DOM 节点列表

**NodeList** 对象是一个从文档中获取的节点列表 (集合) 。

NodeList 对象类似 <a rel="noopener" target="_blank" href="js-htmldom-elements.md">HTMLCollection</a> 对象。

一些旧版本浏览器中的方法（如：**getElementsByClassName()**）返回的是 NodeList 对象，而不是 HTMLCollection 对象。

所有浏览器的  **childNodes** 属性返回的是 NodeList 对象。

大部分浏览器的 **querySelectorAll()** 返回  NodeList 对象。

以下代码选取了文档中所有的 `<p>` 节点：

<!--sec data-title="实例" data-filename="js_dom_nodelist" ces-->
```javascript
var myNodeList = document.querySelectorAll("p");
```

NodeList 中的元素可以通过索引(以 0 为起始位置)来访问。

访问第二个 `<p>` 元素可以是以下代码:

```javascript
y = myNodeList[1];
```
<!--endsec-->

## NodeList 对象 length 属性

NodeList 对象 length 属性定义了节点列表中元素的数量。

<!--sec data-title="实例" data-filename="js_dom_nodelist_length" ces-->
```javascript
var myNodelist = document.querySelectorAll("p");
document.getElementById("demo").innerHTML = myNodelist.length;
```
<!--endsec-->

### 实例解析

获取 `<p>` 元素的集合：

```javascript
var myNodelist = document.querySelectorAll("p");
```

显示节点列表的元素个数：

```javascript
document.getElementById("demo").innerHTML = myNodelist.length;
```

length 属性常用于遍历节点列表。

<!--sec data-title="实例" data-filename="js_dom_nodelist_loop" ces-->
修改节点列表中所有 `<p>` 元素的背景颜色:

```javascript
var myNodelist = document.querySelectorAll("p");
var i;
for (i = 0; i < myNodelist.length; i++) {
    myNodelist[i].style.backgroundColor = "red";
}
```
<!--endsec-->

## HTMLCollection 与 NodeList 的区别

<a rel="noopener" target="_blank" href="js-htmldom-collections.md">HTMLCollection</a> 是 HTML 元素的集合。

NodeList 是一个文档节点的集合。

NodeList 与 HTMLCollection 有很多类似的地方。

NodeList 与 HTMLCollection 都与数组对象有点类似，可以使用索引 (0, 1, 2, 3, 4, ...) 来获取元素。

NodeList 与 HTMLCollection 都有 length 属性。

HTMLCollection 元素可以通过 name，id 或索引来获取。

NodeList 只能通过索引来获取。

只有 NodeList 对象有包含属性节点和文本节点。

> [!NOTE] **节点列表不是一个数组！**
> 节点列表看起来可能是一个数组，但其实不是。
> 你可以像数组一样，使用索引来获取元素。
> 节点列表无法使用数组的方法： valueOf(), pop(), push(), 或 join() 。