# JavaScript 数据类型

**值类型(基本类型)**：字符串（String）、数字(Number)、布尔(Boolean)、对空（Null）、未定义（Undefined）、Symbol。

**引用数据类型**：对象(Object)、数组(Array)、函数(Function)。

> [!INFO]
> 注：Symbol 是 ES6 引入了一种新的原始数据类型，表示独一无二的值。

## JavaScript 拥有动态类型

JavaScript 拥有动态类型。这意味着相同的变量可用作不同的类型：

```javascript
var x;               // x 为 undefined
var x = 5;           // 现在 x 为数字
var x = "John";      // 现在 x 为字符串
```

## JavaScript 字符串

字符串是存储字符（比如 "Bill Gates"）的变量。

字符串可以是引号中的任意文本。您可以使用单引号或双引号：

```javascript
var carname="Volvo XC60";
var carname='Volvo XC60';
```

您可以在字符串中使用引号，只要不匹配包围字符串的引号即可：

<!--sec data-title="实例" data-filename="js_datatypes_string" ces-->
```javascript
var answer="It's alright";
var answer="He is called 'Johnny'";
var answer='He is called "Johnny"';
```
<!--endsec-->

您将在本教程的高级部分学到更多关于字符串的知识。

## JavaScript 数字

JavaScript 只有一种数字类型。数字可以带小数点，也可以不带：

```javascript
var x1=34.00;      //使用小数点来写
var x2=34;         //不使用小数点来写
```

极大或极小的数字可以通过科学（指数）计数法来书写：

<!--sec data-title="实例" data-filename="js_numbers" ces-->
```javascript
var y=123e5;      // 12300000
var z=123e-5;     // 0.00123
```
<!--endsec-->

您将在本教程的高级部分学到更多关于数字的知识。

## JavaScript 布尔

布尔（逻辑）只能有两个值：true 或 false。

```javascript
var x=true;
var y=false;
```

布尔常用在条件测试中。您将在本教程稍后的章节中学到更多关于条件测试的知识。

## JavaScript 数组

下面的代码创建名为 cars 的数组：

```javascript
var cars=new Array();
cars[0]="Saab";
cars[1]="Volvo";
cars[2]="BMW";
```

或者 (condensed array):

```javascript
var cars=new Array("Saab","Volvo","BMW");
```

或者 (literal array):

<!--sec data-title="实例" data-filename="js_datatypes_array" ces-->
```javascript
var cars=["Saab","Volvo","BMW"];
```
<!--endsec-->

数组下标是基于零的，所以第一个项目是 [0]，第二个是 [1]，以此类推。

您将在本教程稍后的章节中学到更多关于数组的知识。

## JavaScript 对象

对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔：

```javascript
var person={firstname:"John", lastname:"Doe", id:5566};
```

上面例子中的对象 (person) 有三个属性：firstname、lastname 以及 id。

空格和折行无关紧要。声明可横跨多行：

```javascript
var person={
firstname : "John",
lastname  : "Doe",
id        :  5566
};
```

对象属性有两种寻址方式：

<!--sec data-title="实例" data-filename="js_datatypes_object" ces-->
```javascript
name=person.lastname;
name=person["lastname"];
```
<!--endsec-->

您将在本教程稍后的章节中学到更多关于对象的知识。

## Undefined 和 Null

Undefined 这个值表示变量不含有值。

可以通过将变量的值设置为 null 来清空变量。

<!--sec data-title="实例" data-filename="js_undefined" ces-->
```javascript
cars=null;
person=null;
```
<!--endsec-->

## 声明变量类型

当您声明新变量时，可以使用关键词 "new" 来声明其类型：

```javascript
var carname=new String;
var x=      new Number;
var y=      new Boolean;
var cars=   new Array;
var person= new Object;
```

> [!TIP]
> JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象。