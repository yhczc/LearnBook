# JavaScript typeof, null, 和 undefined

JavaScript typeof, null, undefined, valueOf()。

## typeof 操作符

你可以使用 typeof 操作符来检测变量的数据类型。

<!--sec data-title="实例" data-filename="js_typeof_typeof" ces-->
```javascript
typeof "John"                 // 返回 string 
typeof  3.14                  // 返回 number
typeof  false                 // 返回 boolean
typeof  [1,2,3,4]             // 返回 object
typeof  {name:'John', age:34} // 返回 object
```

<!--endsec-->
> [!TIP]
> 在JavaScript中，数组是一种特殊的对象类型。 因此 typeof [1,2,3,4] 返回 object。

## null

在 JavaScript 中 null 表示 "什么都没有"。

null是一个只有一个值的特殊类型。表示一个空对象引用。

> [!TIP]
> 用 typeof 检测 null 返回是object。 

你可以设置为 null 来清空对象:

<!--sec data-title="实例" data-filename="js_typeof_null" ces-->
```javascript
var
person = null;           // 值为 null(空), 但类型为对象
```
<!--endsec-->

你可以设置为 undefined 来清空对象:

<!--sec data-title="实例" data-filename="js_typeof_undefined_1" ces-->
```javascript
var
person = undefined;     // 值为 undefined, 类型为undefined
```
<!--endsec-->

## undefined

在 JavaScript 中, **undefined** 是一个没有设置值的变量。

**typeof** 一个没有值的变量会返回 undefined。

<!--sec data-title="实例" data-filename="js_typeof_undefined" ces-->
```javascript
var person;                  // 值为 undefined(空), 类型是undefined
```
<!--endsec-->

任何变量都可以通过设置值为 **undefined** 来清空。类型为 **undefined**.

<!--sec data-title="实例" data-filename="js_typeof_undefined_2" ces-->
```javascript
person = undefined;          // 值为 undefined, 类型是undefined
```
<!--endsec-->

## undefined 和 null 的区别

<!--sec data-title="实例" data-filename="js_typeof_undefined_3" ces-->
null 和 undefined 的值相等，但类型不等：

```javascript
typeof undefined            // undefined
typeofnull                  // object
null === undefined          // false
null == undefined           // true
```
<!--endsec-->

