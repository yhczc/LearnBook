# JavaScript 保留关键字

在 JavaScript 中，一些标识符是保留关键字，不能用作变量名或函数名。

## JavaScript 标准

所有的现代浏览器完全支持 ECMAScript 3（ES3，JavaScript 的第三版，从 1999 年开始）。

ECMAScript 4（ES4）未通过。

ECMAScript 5（ES5，2009 年发布），是 JavaScript 最新的官方版本。

随着时间的推移，我们开始看到，所有的现代浏览器已经完全支持 ES5。

## JavaScript 保留关键字

Javascript 的保留关键字不可以用作变量、标签或者函数名。有些保留关键字是作为 Javascript 以后扩展使用。

<table>
<tbody>
<tr>
<td>abstract</td>
<td>arguments</td>
<td>boolean</td>
<td>break</td>
<td>byte</td>
</tr>
<tr>
<td>case</td>
<td>catch</td>
<td>char</td>
<td>class*</td>
<td>const</td>
</tr>
<tr>
<td>continue</td>
<td>debugger</td>
<td>default</td>
<td>delete</td>
<td>do</td>
</tr>
<tr>
<td>double</td>
<td>else</td>
<td>enum*</td>
<td>eval</td>
<td>export*</td>
</tr>
<tr>
<td>extends*</td>
<td>false</td>
<td>final</td>
<td>finally</td>
<td>float</td>
</tr>
<tr>
<td>for</td>
<td>function</td>
<td>goto</td>
<td>if</td>
<td>implements</td>
</tr>
<tr>
<td>import*</td>
<td>in</td>
<td>instanceof</td>
<td>int</td>
<td>interface</td>
</tr>
<tr>
<td>let</td>
<td>long</td>
<td>native</td>
<td>new</td>
<td>null</td>
</tr>
<tr>
<td>package</td>
<td>private</td>
<td>protected</td>
<td>public</td>
<td>return</td>
</tr>
<tr>
<td>short</td>
<td>static</td>
<td>super*</td>
<td>switch</td>
<td>synchronized</td>
</tr>
<tr>
<td>this</td>
<td>throw</td>
<td>throws</td>
<td>transient</td>
<td>true</td>
</tr>
<tr>
<td>try</td>
<td>typeof</td>
<td>var</td>
<td>void</td>
<td>volatile</td>
</tr>
<tr>
<td>while</td>
<td>with</td>
<td>yield</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

\* 标记的关键字是 ECMAScript5 中新添加的。

## JavaScript 对象、属性和方法

您也应该避免使用 JavaScript 内置的对象、属性和方法的名称作为 Javascript 的变量或函数名：

<table>
<tbody><tr>
<td>Array</td>
<td>Date</td>
<td>eval</td>
<td>function</td>
<td>hasOwnProperty</td>
</tr>
<tr>
<td>Infinity</td>
<td>isFinite</td>
<td>isNaN</td>
<td>isPrototypeOf</td>
<td>length</td>
</tr>
<tr>
<td>Math</td>
<td>NaN</td>
<td>name</td>
<td>Number</td>
<td>Object</td>
</tr>
<tr>
<td>prototype</td>
<td>String</td>
<td>toString</td>
<td>undefined</td>
<td>valueOf</td>
</tr>
</tbody>
</table>

## Java 保留关键字

JavaScript 经常与 Java 一起使用。您应该避免使用一些 Java 对象和属性作为 JavaScript 标识符：

<table>
<tbody><tr>
<td>getClass</td>
<td>java</td>
<td>JavaArray</td>
<td>javaClass</td>
<td>JavaObject</td>
<td>JavaPackage</td>
</tr>
</tbody>
</table>

## Windows 保留关键字

JavaScript 可以在 HTML 外部使用。它可在许多其他应用程序中作为编程语言使用。

在 HTML 中，您必须（为了可移植性，您也应该这么做）避免使用 HTML 和 Windows 对象和属性的名称作为 Javascript 的变量及函数名：

<table>
<tbody><tr>
<td>alert</td>
<td>all</td>
<td>anchor</td>
<td>anchors</td>
<td>area</td>
</tr>
<tr>
<td>assign</td>
<td>blur</td>
<td>button</td>
<td>checkbox</td>
<td>clearInterval</td>
</tr>
<tr>
<td>clearTimeout</td>
<td>clientInformation</td>
<td>close</td>
<td>closed</td>
<td>confirm</td>
</tr>
<tr>
<td>constructor</td>
<td>crypto</td>
<td>decodeURI</td>
<td>decodeURIComponent</td>
<td>defaultStatus</td>
</tr>
<tr>
<td>document</td>
<td>element</td>
<td>elements</td>
<td>embed</td>
<td>embeds</td>
</tr>
<tr>
<td>encodeURI</td>
<td>encodeURIComponent</td>
<td>escape</td>
<td>event</td>
<td>fileUpload</td>
</tr>
<tr>
<td>focus</td>
<td>form</td>
<td>forms</td>
<td>frame</td>
<td>innerHeight</td>
</tr>
<tr>
<td>innerWidth</td>
<td>layer</td>
<td>layers</td>
<td>link</td>
<td>location</td>
</tr>
<tr>
<td>mimeTypes</td>
<td>navigate</td>
<td>navigator</td>
<td>frames</td>
<td>frameRate</td>
</tr>
<tr>
<td>hidden</td>
<td>history</td>
<td>image</td>
<td>images</td>
<td>offscreenBuffering</td>
</tr>
<tr>
<td>open</td>
<td>opener</td>
<td>option</td>
<td>outerHeight</td>
<td>outerWidth</td>
</tr>
<tr>
<td>packages</td>
<td>pageXOffset</td>
<td>pageYOffset</td>
<td>parent</td>
<td>parseFloat</td>
</tr>
<tr>
<td>parseInt</td>
<td>password</td>
<td>pkcs11</td>
<td>plugin</td>
<td>prompt</td>
</tr>
<tr>
<td>propertyIsEnum</td>
<td>radio</td>
<td>reset</td>
<td>screenX</td>
<td>screenY</td>
</tr>
<tr>
<td>scroll</td>
<td>secure</td>
<td>select</td>
<td>self</td>
<td>setInterval</td>
</tr>
<tr>
<td>setTimeout</td>
<td>status</td>
<td>submit</td>
<td>taint</td>
<td>text</td>
</tr>
<tr>
<td>textarea</td>
<td>top</td>
<td>unescape</td>
<td>untaint</td>
<td>window</td>
</tr>
</tbody>
</table>

## HTML 事件句柄

除此之外，您还应该避免使用 HTML 事件句柄的名称作为 Javascript 的变量及函数名。

实例：

<table>
<tbody>
<tr>
<td>onblur</td>
<td>onclick</td>
<td>onerror</td>
<td>onfocus</td>
</tr>
<tr>
<td>onkeydown</td>
<td>onkeypress</td>
<td>onkeyup</td>
<td>onmouseover</td>
</tr>
<tr>
<td>onload</td>
<td>onmouseup</td>
<td>onmousedown</td>
<td>onsubmit</td>
</tr><tr>
</tr>
</tbody>
</table>

## 非标准 JavaScript

除了保留关键字，在 JavaScript 实现中也有一些非标准的关键字。

一个实例是 **const** 关键字，用于定义变量。
一些 JavaScript 引擎把 const 当作 var 的同义词。另一些引擎则把 const 当作只读变量的定义。

Const 是 JavaScript 的扩展。JavaScript 引擎支持它用在 Firefox 和 Chrome 中。但是它并不是 JavaScript 标准 ES3
或 ES5 的组成部分。**建议：不要使用它**。

