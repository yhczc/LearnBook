# JavaScript prototype（原型对象）

所有的 JavaScript 对象都会从一个 prototype（原型对象）中继承属性和方法。

在前面的章节中我们学会了如何使用对象的构造器（constructor）：

<!--sec data-title="实例" data-filename="js_object_prototype1" ces-->
```javascript
function Person(first, last, age, eyecolor) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eyecolor;
}
var myFather = newPerson("John", "Doe", 50, "blue");
var myMother = newPerson("Sally", "Rally", 48, "green");
```
<!--endsec-->

我们也知道在一个已存在的对象构造器中是不能添加新的属性的：

<!--sec data-title="实例" data-filename="js_object_prototype3" ces-->
```javascript
Person.nationality = "English";
```
<!--endsec-->

要添加一个新的属性需要在在构造器函数中添加：

<!--sec data-title="实例" data-filename="js_object_prototype4" ces-->
```javascript
function Person(first, last, age, eyecolor) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eyecolor;
    this.nationality = "English";
}
```
<!--endsec-->

## prototype 继承

所有的 JavaScript 对象都会从一个 prototype（原型对象）中继承属性和方法：

- `Date` 对象从 `Date.prototype` 继承。
- `Array` 对象从 `Array.prototype` 继承。
- `Person` 对象从 `Person.prototype` 继承。

所有 JavaScript 中的对象都是位于原型链顶端的 Object 的实例。

JavaScript 对象有一个指向一个原型对象的链。当试图访问一个对象的属性时，它不仅仅在该对象上搜寻，还会搜寻该对象的原型，以及该对象的原型的原型，依次层层向上搜索，直到找到一个名字匹配的属性或到达原型链的末尾。

`Date` 对象, `Array` 对象, 以及 `Person` 对象从 `Object.prototype` 继承。

### 添加属性和方法

有的时候我们想要在所有已经存在的对象添加新的属性或方法。

另外，有时候我们想要在对象的构造函数中添加属性或方法。

使用 prototype 属性就可以给对象的构造函数添加新的属性：

<!--sec data-title="实例" data-filename="js_object_prototype5" ces-->
```javascript
function Person(first, last, age, eyecolor) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eyecolor;
}
Person.prototype.nationality = "English";
```
<!--endsec-->

当然我们也可以使用 prototype 属性就可以给对象的构造函数添加新的方法：

<!--sec data-title="实例" data-filename="js_object_prototype6" ces-->
```javascript
function Person(first, last, age, eyecolor) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eyecolor;
}
Person.prototype.name = function() {
    return this.firstName + "" + this.lastName;
};
```
<!--endsec-->