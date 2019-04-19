# JavaScript while 循环

只要指定条件为 true，循环就可以一直执行代码块。

## while 循环

while 循环会在指定条件为真时循环执行代码块。

### 语法

```
while (条件)
{   
    需要执行的代码
}
```

### 实例

本例中的循环将继续运行，只要变量 i 小于 5：

<!--sec data-title="实例" data-filename="js_while" ces-->
```javascript
while (i < 5) {
    x = x + "The number is " + i + " <br> ";
    i++;
}
```
<!--endsec-->

> [!TIP]
> 如果您忘记增加条件中所用变量的值，该循环永远不会结束。这可能导致浏览器崩溃。

## do/while 循环

do/while 循环是 while 循环的变体。该循环会在检查条件是否为真之前执行一次代码块，然后如果条件为真的话，就会重复这个循环。

### 语法

```
do
{   
    需要执行的代码
}
while (条件);
```

### 实例

下面的例子使用 do/while 循环。该循环至少会执行一次，即使条件为 false 它也会执行一次，因为代码块会在条件被测试前执行：

<!--sec data-title="实例" data-filename="js_dowhile" ces-->
```javascript
do {
    x = x + "The number is " + i + " <br>";
    i++;
} while (i < 5);
```
<!--endsec-->

别忘记增加条件中所用变量的值，否则循环永远不会结束！

## 比较 for 和 while

如果您已经阅读了前面那一章关于 for 循环的内容，您会发现 while 循环与 for 循环很像。

本例中的循环使用 for 循环来显示 cars 数组中的所有值：

<!--sec data-title="实例" data-filename="js_loop_for_cars" ces-->
```javascript
cars = [ " BMW ", " Volvo ", " Saab ", " Ford "];
vari = 0;
for (; cars[i];) {
    document.write(cars[i] + "<br>");
    i++;
}
```
<!--endsec-->

本例中的循环使用 **while 循环**来显示 cars 数组中的所有值：

<!--sec data-title="实例" data-filename="js_loop_while_cars" ces-->
```javascript
cars = [ " BMW ", " Volvo ", " Saab ", " Ford "];
vari = 0;
while (cars[i]) {
    document.write(cars[i] + "<br>");
    i++;
}
```
<!--endsec-->

