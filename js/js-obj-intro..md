# JavaScript 对象

JavaScript 对象是拥有属性和方法的数据。

## 真实生活中的对象，

真实生活中，一辆汽车是一个对象。

对象有它的属性，如重量和颜色等，方法有启动停止等:

| 对象  | 属性  | 方法  |
| :------------ | :------------ | :------------ |
| <img src="img/objectExplained.gif" style="width:368px;height:230px">  | `car.name = Fiat` <br><br> `car.model = 500` <br><br> `car.weight = 850kg` <br><br> `car.color = white`  |`car.start()` <br><br> `car.drive()` <br><br> `car.brake()` <br><br> `car.stop()`  |

所有汽车都有这些属性，但是每款车的属性都不尽相同。

所有汽车都拥有这些方法，但是它们被执行的时间都不尽相同。

## JavaScript 对象

在 JavaScript中，几乎所有的事物都是对象。

> [!TIP]
> 在 JavaScript 中，对象是非常重要的，当你理解了对象，就可以了解 JavaScript 。
你已经学习了 JavaScript 变量的赋值。

以下代码为变量 **car** 设置值为 "Fiat" :

```javascript
var car = "Fiat";
```

对象也是一个变量，但对象可以包含多个值（多个变量）。

```javascript
var car = {type:"Fiat", model:500, color:"white"};
```

在以上实例中，3 个值 ("Fiat", 500, "white") 赋予变量 car。

在以上实例中，3 个变量 (type, model, color) 赋予变量 car。

> [!TIP]
> JavaScript 对象是变量的容器。

## 对象定义

你可以使用字符来定义和创建 JavaScript 对象:

<!--sec data-title="实例" data-filename="js_object_create_1" ces-->
```javascript
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```
<!--endsec-->

定义 JavaScript 对象可以跨越多行，空格跟换行不是必须的：
