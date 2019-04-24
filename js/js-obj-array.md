# JavaScript Array（数组） 对象

数组对象的作用是：使用单独的变量名来存储一系列的值。

## 在线实例

创建数组, 为其赋值：

<!--sec data-title="实例" data-filename="js_array" ces-->
```javascript
var mycars = new Array();
mycars[0] = "Saab";
mycars[1] = "Volvo";
mycars[2] = "BMW";
```
<!--endsec-->

页面底部你可以找到更多的实例。

## 什么是数组?

数组对象是使用单独的变量名来存储一系列的值。

如果你有一组数据（例如：车名字），存在单独变量如下所示：

```
var
car1="Saab";
var
car2="Volvo";
var
car3="BMW";
```

然而，如果你想从中找出某一辆车？并且不是3辆，而是300辆呢？这将不是一件容易的事！

最好的方法就是用数组。

数组可以用一个变量名存储所有的值，并且可以用变量名访问任何一个值。

数组中的每个元素都有自己的的ID，以便它可以很容易地被访问到。

## 创建一个数组

创建一个数组，有三种方法。 

下面的代码定义了一个名为  myCars的数组对象：

1: 常规方式:

```javascript
var myCars=new Array();
myCars[0]="Saab";
myCars[1]="Volvo";
myCars[2]="BMW";
```

2: 简洁方式:

```javascript
var myCars=new Array("Saab","Volvo","BMW");
```

3: 字面:

```javascript
var myCars=["Saab","Volvo","BMW"];
```

## 访问数组

通过指定数组名以及索引号码，你可以访问某个特定的元素。

以下实例可以访问myCars数组的第一个值：

```javascript
var
name=myCars[0];
```

以下实例修改了数组 myCars 的第一个元素:

```javascrip
myCars[0]="Opel";
```

> [!TIP]
> [0] 是数组的第一个元素。[1] 是数组的第二个元素。

## 在一个数组中你可以有不同的对象

所有的JavaScript变量都是对象。数组元素是对象。函数是对象。

因此，你可以在数组中有不同的变量类型。

你可以在一个数组中包含对象元素、函数、数组：

```javascript
myArray[0]=Date.now;
myArray[1]=myFunction;
myArray[2]=myCars;
```

## 数组方法和属性

使用数组对象预定义属性和方法：

```javascript
var x=myCars.length             // myCars 中元素的数量
var y=myCars.indexOf("Volvo")   // "Volvo" 值的索引值
```

## 完整的数组对象参考手册

你可以参考本站关于数组的所有属性和方法的完整参考手册。

参考手册包含了所有属性和方法的描述（和更多的例子）。

<a href="jsref-obj-array.md">完整数组对象参考手册</a>

## 创建新方法

原型是JavaScript全局构造函数。它可以构建新Javascript对象的属性和方法。

<!--sec data-title="实例：创建一个新的方法。" data-filename="js_prototype_array" ces-->
```javascript
Array.prototype.myUcase=function(){
    for (i=0;i<this.length;i++){
        this[i]=this[i].toUpperCase();
    }
}
```
<!--endsec-->

上面的例子创建了新的数组方法用于将数组小写字符转为大写字符。

## 更多实例

<a target="_blank" href="/run/run.html#filename=tryjsref_concat">合并两个数组 - concat()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_concat2">合并三个数组 - concat()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_join">用数组的元素组成字符串 - join()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_pop">删除数组的最后一个元素 - pop()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_push">数组的末尾添加新的元素 - push()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_reverse">将一个数组中的元素的顺序反转排序 - reverse()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_shift">删除数组的第一个元素 - shift()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_slice_array">从一个数组中选择元素 - slice()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_sort">数组排序（按字母顺序升序）- sort()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_sort2">数字排序（按数字顺序升序）- sort()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_sort3">数字排序（按数字顺序降序）- sort()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_splice">在数组的第2位置添加一个元素 - splice()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_tostring_array">转换数组到字符串 -tostring()</a>

<a target="_blank" href="/run/run.html#filename=tryjsref_unshift">在数组的开头添加新元素 - unshift()</a>