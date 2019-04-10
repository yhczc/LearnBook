# JavaScript 注释

JavaScript 注释可用于提高代码的可读性。

## JavaScript 注释

JavaScript 不会执行注释。

我们可以添加注释来对 JavaScript 进行解释，或者提高代码的可读性。

单行注释以 `//` 开头。

本例用单行注释来解释代码：

<!--sec data-title="实例" data-filename="js_comments1" ces-->
```javascript
// 输出标题：
document.getElementById("myH1").innerHTML="欢迎来到我的主页";
// 输出段落：
document.getElementById("myP").innerHTML="这是我的第一个段落。";
```
<!--endsec-->

## JavaScript 多行注释

多行注释以 `/*` 开始，以 `*/` 结尾。

下面的例子使用多行注释来解释代码：

<!--sec data-title="实例" data-filename="js_comments2" ces-->
```javascript
/*
下面的这些代码会输出
一个标题和一个段落
并将代表主页的开始
*/
document.getElementById("myH1").innerHTML="欢迎来到我的主页";
document.getElementById("myP").innerHTML="这是我的第一个段落。";
```
<!--endsec-->

## 使用注释来阻止执行

在下面的例子中，注释用于阻止其中一条代码行的执行（可用于调试）：

<!--sec data-title="实例" data-filename="js_comments3" ces-->
```javascript
// document.getElementById("myH1").innerHTML="欢迎来到我的主页";
document.getElementById("myP").innerHTML="这是我的第一个段落。";
```
<!--endsec-->

在下面的例子中，注释用于阻止代码块的执行（可用于调试）：

<!--sec data-title="实例" data-filename="js_comments4" ces-->
```javascript
/*
document.getElementById("myH1").innerHTML="欢迎来到我的主页";
document.getElementById("myP").innerHTML="这是我的第一个段落。";
*/
```
<!--endsec-->

## 在行末使用注释

在下面的例子中，我们把注释放到代码行的结尾处：

<!--sec data-title="实例" data-filename="js_comments5" ces-->
```javascript
var x=5;    // 声明 x 并把 5 赋值给它
var y=x+2;  // 声明 y 并把 x+2 赋值给它
```
<!--endsec-->