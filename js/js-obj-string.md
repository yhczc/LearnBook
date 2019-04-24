# JavaScript 字符串（String） 对象

String 对象用于处理已有的字符块。

## JavaScript 字符串

一个字符串用于存储一系列字符就像 "John Doe".

一个字符串可以使用单引号或双引号：

```javascript
var carname="Volvo XC60";
var carname='Volvo XC60';
```

你使用位置（索引）可以访问字符串中任何的字符：

```javascript
var character=carname[7];
```

字符串的索引从零开始, 所以字符串第一字符为 [0],第二个字符为 [1], 等等。

你可以在字符串中使用引号，如下实例：

```javascript
var answer="It's alright";
var answer="He is called 'Johnny'";
var answer='He is called "Johnny"';
```

或者你可以在字符串中使用转义字符(\)使用引号：

<!--sec data-title="实例" data-filename="js_datatypes_string" ces-->
```javascript
var answer='It\'s alright';
var answer="He is called \"Johnny\"";
```
<!--endsec-->

## 字符串（String）

字符串（String）使用长度属性**length**来计算字符串的长度：

<!--sec data-title="实例" data-filename="js_string_length" ces-->
```javascript
var txt="Hello World!";
document.write(txt.length);

var txt="ABCDEFGHIJKLMNOPQRSTUVWXYZ";
document.write(txt.length);
```
<!--endsec-->

## 在字符串中查找字符串

字符串使用 indexOf() 来定位字符串中某一个指定的字符首次出现的位置：

<!--sec data-title="实例" data-filename="js_string_indexof" ces-->
```javascript
var str="Hello world, welcome to the universe.";
var n=str.indexOf("welcome");
```
<!--endsec-->

如果没找到对应的字符函数返回-1

lastIndexOf() 方法在字符串末尾开始查找字符串出现的位置。

## 内容匹配

**match()**函数用来查找字符串中特定的字符，并且如果找到的话，则返回这个字符。

<!--sec data-title="实例" data-filename="js_string_match" ces-->
```javascript
var str="Hello world!";
document.write(str.match("world") + "<br>");
document.write(str.match("World") + "<br>");
document.write(str.match("world!"));
```
<!--endsec-->

## 替换内容

**replace()** 方法在字符串中用某些字符替换另一些字符。

<!--sec data-title="实例" data-filename="js_string_replace" ces-->
```javascript
str="Please visit Microsoft!"
var n=str.replace("Microsoft","Gitmt");
```
<!--endsec-->

## 字符串大小写转换

字符串大小写转换使用函数 **toUpperCase() **/** toLowerCase()**:

<!--sec data-title="实例" data-filename="js_string_toupper" ces-->
```javascript
var txt="Hello World!";       // String
var txt1=txt.toUpperCase();   // txt1 文本会转换为大写
var txt2=txt.toLowerCase();   // txt2 文本会转换为小写
```
<!--endsec-->

## 字符串转为数组

字符串使用**split()**函数转为数组:

<!--sec data-title="实例" data-filename="js_string_split" ces-->
```javascript
txt="a,b,c,d,e"   // String
txt.split(",");   // 使用逗号分隔
txt.split(" ");   // 使用空格分隔
txt.split("|");   // 使用竖线分隔
```
<!--endsec-->

## 特殊字符

Javascript 中可以使用反斜线（\）插入特殊符号，如：撇号,引号等其他特殊符号。

查看如下 JavaScript 代码:

```javascript
var txt="We are the so-called "Vikings" from the north.";
document.write(txt);
```

在JavaScript中，字符串的开始和停止使用单引号或双引号。这意味着，上面的字符串将被切成： We are the so-called

解决以上的问题可以使用反斜线来转义引号：

```javascript
var txt="We are the so-called \"Vikings\" from the north.";
document.write(txt);
```

JavaScript将输出正确的文本字符串：We are the so-called "Vikings" from the north.

下表列出其他特殊字符，可以使用反斜线转义特殊字符：

| 代码 | 输出 |
| :------------  | :------------ |
| \' | 单引号 |
| \" | 双引号 |
| \\ | 斜杆 |
| \n | 换行 |
| \r | 回车 |
| \t | tab |
| \b | 空格 |
| \f | 换页 |
## 字符串属性和方法

属性:

- length
- prototype
- constructor

方法:

- charAt()
- charCodeAt()
- concat()
- fromCharCode()
- indexOf()
- lastIndexOf()
- match()
- replace()
- search()
- slice()
- split()
- substr()
- substring()
- toLowerCase()
- toUpperCase()
- valueOf()

更多方法与属性介绍可以参考：<a rel="noopener" target="_blank" href="../jsref/jsref-obj-string.md">JavaScript String 对象</a>