# JavaScript 简介

- JavaScript 是互联网上最流行的脚本语言，这门语言可用于 HTML 和 web，更可广泛用于服务器、PC、笔记本电脑、平板电脑和智能手机等设备。
- JavaScript 是脚本语言。
- JavaScript 是一种轻量级的编程语言。
- JavaScript 是可插入 HTML 页面的编程代码。
- JavaScript 插入 HTML 页面后，可由所有的现代浏览器执行。
- JavaScript 很容易学习。
## 您将学到什么

下面是您将在本教程中学到的主要内容。

## JavaScript：直接写入 HTML 输出流

<!--sec data-title="实例" data-url='http://www.baidu.com' ces-->

```javascript
document.write("<h1>这是一个标题</h1>");
document.write("<p>这是一个段落。</p>");
```
<!--endsec-->


实例
```
{% codeeditor src='../js/demo/js_intro_document_write.html' %}
{% endcodeeditor %}
```


>[!TIP]
> 您只能在 HTML 输出中使用 document.write。如果您在文档加载后使用该方法，会覆盖整个文档。

## JavaScript：对事件的反应

实例
```html
<button type="button" onclick="alert('欢迎!')">点我!</button>
```

尝试一下 »

