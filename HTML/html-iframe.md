# HTML 框架 
通过使用框架，你可以在同一个浏览器窗口中显示不止一个页面。
<iframe src="/index.html"></iframe>
**iframe语法:**
```html
<iframe src="URL"></iframe>
```
该URL指向不同的网页。
## Iframe - 设置高度与宽度
height 和 width 属性用来定义iframe标签的高度与宽度。  
属性默认以像素为单位, 但是你可以指定其按比例显示 (如："80%")。
```html
<iframe src="demo_iframe.htm" width="200" height="200"></iframe>
```
## Iframe - 移除边框
frameborder 属性用于定义iframe表示是否显示边框。  
设置属性值为 "0" 移除iframe的边框:
```html
<iframe src="demo_iframe.htm" frameborder="0"></iframe>
```
## 使用iframe来显示目标链接页面
iframe可以显示一个目标链接的页面  
目标链接的属性必须使用iframe的属性，如下实例:
```html
<iframe src="demo_iframe.htm" name="iframe_a"></iframe>
<p><a href="http://www.tepuw.com" target="iframe_a">TEPUW.COM</a></p>
```
## HTML iframe 标签
| 标签  | 说明  |
| ------------ | ------------ |
| `<iframe>`  | 定义一个内联的iframe  |
