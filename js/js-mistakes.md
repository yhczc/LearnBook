# JavaScript 使用误区

本章节我们将讨论 JavaScript 的使用误区。

## 赋值运算符应用错误

在 JavaScript 程序中如果你在 if 条件语句中使用赋值运算符的等号 (=) 将会产生一个错误结果, 正确的方法是使用比较运算符的两个等号
(==)。

**if** 条件语句返回 **false** (是我们预期的)因为 x 不等于 10:

<!--sec data-title="实例" data-filename="js_mistakes_equal_1" ces-->
```javascript
var x = 0;
if (x == 10)
```
<!--endsec-->

**if** 条件语句返回 **true** (不是我们预期的)因为条件语句执行为 x 赋值 10，10 为 true:

<!--sec data-title="实例" data-filename="js_mistakes_equal_2" ces-->
```javascript
var x = 0;
if (x = 10)
```
<!--endsec-->

**if** 条件语句返回 **false** (不是我们预期的)因为条件语句执行为 x 赋值 0，0 为 false:

<!--sec data-title="实例" data-filename="js_mistakes_equal_3" ces-->
```javascript
var x = 0;
if (x = 0)
```
<!--endsec-->

> [!TIP]
> 赋值语句返回变量的值。

## 比较运算符常见错误

在常规的比较中，数据类型是被忽略的，以下 if 条件语句返回 true：

<!--sec data-title="实例" data-filename="js_mistakes_loose_1" ces-->
```javascript
var x = 10;
var y = "10";
if (x == y)
```
<!--endsec-->

在严格的比较运算中，=== 为恒等计算符，同时检查表达式的值与类型，以下  if 条件语句返回 false：

<!--sec data-title="实例" data-filename="js_mistakes_loose_2" ces-->
```javascript
var x = 10;
var y = "10";
if (x === y)
```
<!--endsec-->

这种错误经常会在 switch 语句中出现，switch 语句会使用恒等计算符(===)进行比较:

以下实例会执行 alert 弹窗：

<!--sec data-title="实例" data-filename="js_mistakes_loose_3" ces-->
```javascript
var x = 10;
switch (x) {
   case 10: alert("Hello");
}
```
<!--endsec-->

以下实例由于类型不一致不会执行 alert 弹窗：

<!--sec data-title="实例" data-filename="js_mistakes_loose_4" ces-->
```javascript
var x = 10;
switch (x) {
case "10":
    alert("Hello");
}
```
<!--endsec-->

## 加法与连接注意事项

**加法**是两个**数字**相加。

**连接**是两个**字符串**连接。

JavaScript 的加法和连接都使用 + 运算符。

接下来我们可以通过实例查看两个数字相加及数字与字符串连接的区别：

<!--sec data-title="实例" data-filename="js_mistakes_add_1" ces-->
```javascript
var x = 10 + 5;          //x的结果为15
var x = 10 + "5";        // x 的结果为 "105"
```
<!--endsec-->

使用变量相加结果也不一致:

<!--sec data-title="实例" data-filename="js_mistakes_add_2" ces-->
```javascript
var x = 10;
var y = 5;
var z = x + y;          // z 的结果为 15
var x = 10;
var y = "5";
var z =     x + y;      // z 的结果为 "105"
```
<!--endsec-->

## 浮点型数据使用注意事项

JavaScript 中的所有数据都是以 64 位**浮点型数据(float)** 来存储。

所有的编程语言，包括 JavaScript，对浮点型数据的精确度都很难确定：

<!--sec data-title="实例" data-filename="js_mistakes_floats" ces-->
```javascript
var x = 0.1;
var y = 0.2;
var z = x + y            // z 的结果为 0.3
if (z == 0.3)            // 返回 false
```
<!--endsec-->

为解决以上问题，可以用整数的乘除法来解决：

<!--sec data-title="实例" data-filename="js_mistakes_floats_ok" ces-->
```javascript
var z = (x * 10 + y * 10) / 10;       // z 的结果为 0.3
```
<!--endsec-->

更多内容可以参考：[JavaScript 中精度问题以及解决方案](../w3cnote/js-precision-problem-and-solution.html "JavaScript 中精度问题以及解决方案")

## JavaScript 字符串分行

JavaScript 允许我们在字符串中使用断行语句:

<!--sec data-title="实例1" data-filename="js_mistakes_string_1" ces-->
```javascript
var x = "Hello World!";
```
<!--endsec-->

但是，在字符串中直接使用回车换行是会报错的：

<!--sec data-title="实例2" data-filename="js_mistakes_string_2" ces-->
```javascript
var x = "HelloWorld!";
```
<!--endsec-->

我们可以在选择开发工具或按下 F12 来查看错误信息：



字符串断行需要使用反斜杠(\)，如下所示:

<!--sec data-title="实例3" data-filename="js_mistakes_string_3" ces-->
```javascript
var x = "Hello \World!";
```
<!--endsec-->

## 错误的使用分号

以下实例中，if 语句失去方法体，原 if 语句的方法体作为独立的代码块被执行，导致错误的输出结果。

由于分号使用错误，if 语句中的代码块就一定会执行：

<!--sec data-title="实例" data-filename="js_mistakes_semicolon" ces-->
```javascript
if (x == 19);
{
    // code block
}
```
<!--endsec-->

## Return 语句使用注意事项

JavaScript 默认是在代码的最后一行自动结束。

以下两个实例返回结果是一样的(一个有分号一个没有):

<!--sec data-title="实例1" data-filename="js_mistakes_return_1" ces-->
```javascript
function myFunction(a) {
    var power = 10
    return a * power
}
```
<!--endsec-->

<!--sec data-title="实例2" data-filename="js_mistakes_return_2" ces-->
```javascript
function myFunction(a) {
    var power = 10;
    return a * power;
}
```
<!--endsec-->

JavaScript 也可以使用多行来结束一个语句。

以下实例返回相同的结果:

<!--sec data-title="实例3" data-filename="js_mistakes_return_3" ces-->
```javascript
function myFunction(a) {
    var   power = 10;
    return a * power;
}
```
<!--endsec-->

但是，以下实例结果会返回 **undefined**：

<!--sec data-title="实例" data-filename="js_mistakes_return_4" ces-->
```javascript
function myFunction(a) {
    var   power = 10;
    return    a * power;
}
```
<!--endsec-->

为什么会有这样的结果呢？因为在 JavaScript 中，实例 4 的代码与下面的代码一致：

### 解析


如果是一个不完整的语句，如下所示:

```javascript
var
```

JavaScript 将尝试读取第二行的语句：

```javascript
power = 10;
```

但是由于这样的语句是完整的:

```javascript
return
```

JavaScript 将自动关闭语句:

```javascript
return;
```

在 JavaScript 中，分号是可选的 。

由于 return 是一个完整的语句，所以 JavaScript 将关闭 return 语句。

> [!TIP]
> **注意：**不用对 return 语句进行断行。

## 数组中使用名字来索引

许多程序语言都允许使用名字来作为数组的索引。

使用名字来作为索引的数组称为关联数组(或哈希)。

JavaScript 不支持使用名字来索引数组，只允许使用数字索引。

<!--sec data-title="实例" data-filename="js_array_associative_1" ces-->
```javascript
var person = [];
person[0] = "John";
person[1] = "Doe";
person[2] = 46;
var x = person.length;         // person.length 返回 3
var y = person[0];             // person[0] 返回 "John"
```
<!--endsec-->

在 JavaScript 中, **对象** 使用 **名字作为索引**。

如果你使用名字作为索引，当访问数组时，JavaScript 会把数组重新定义为标准对象。

执行这样操作后，数组的方法及属性将不能再使用，否则会产生错误:

<!--sec data-title="实例" data-filename="js_array_associative_2" ces-->
```javascript
var person = [];
person["firstName"] = "John";
person["lastName"] = "Doe";
person["age"] = 46;
var x = person.length;         // person.length 返回 0
var y = person[0];             // person[0] 返回 undefined
```
<!--endsec-->

## 定义数组元素，最后不能添加逗号

添加逗号虽然语法没有问题，但是在不同的浏览器可能得到不同的结果。

```javascript
var colors = [5, 6, 7,]; //这样数组的长度可能为3 也可能为4。
```

正确的定义方式：
```javascript
points = [40, 100, 1, 5, 25, 10];
```

## 定义对象，最后不能添加逗号

错误的定义方式：

```
websites = {site:"马桶教程", url:"www.gitmt.com", like:460,}
```

正确的定义方式：

```javascript
websites = {site:"马桶教程", url:"www.gitmt.com", like:460}
```
## Undefined 不是 Null

在 JavaScript 中, **null** 用于对象, **undefined** 用于变量，属性和方法。

对象只有被定义才有可能为 null，否则为 undefined。

如果我们想测试对象是否存在，在对象还没定义时将会抛出一个错误。

错误的使用方式：

```javascript
if (myObj !== null && typeof myObj !== "undefined")
```

正确的方式是我们需要先使用 typeof 来检测对象是否已定义：

```javascript
if (typeof myObj !== "undefined" && myObj !== null)
```

## 程序块作用域

在每个代码块中 JavaScript 不会创建一个新的作用域，一般各个代码块的作用域都是全局的。

以下代码的的变量 i 返回 10，而不是 undefined：

<!--sec data-title="实例" data-filename="js_mistakes_scope" ces-->
```javascript
for (var i = 0; i < 10; i++) {
// some code
}
return i;
```
<!--endsec-->