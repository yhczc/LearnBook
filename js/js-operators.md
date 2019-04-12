# JavaScript 运算符

**运算符 = 用于赋值。**

**运算符 + 用于加值。**

------------

运算符 = 用于给 JavaScript 变量赋值。

算术运算符 + 用于把值加起来。

<!--sec data-title="实例" data-filename="js_operators1" ces-->
指定变量值，并将值相加：
```javascript
y=5;
z=2;
x=y+z;
```
在以上语句执行后，x 的值是：
```javascript
7
```
<!--endsec-->

## JavaScript 算术运算符

y=5，下面的表格解释了这些算术运算符：

| 运算符  | 描述  | 例子  | x 运算结果  | y 运算结果  | 在线实例  |
| :------ | :------ | :------ | :------ | :------ | ------ |
| +  | 加法  | x=y+2  | 7  | 5  | [实例](../run/run.html#filename=js_oper_add "实例")  |
| -  | 减法  | x=y-2  | 3  | 5  | [实例](../run/run.html#filename=js_oper_sub "实例")  |
| *  | 乘法  | `x=y*2`  | 10  | 5  | [实例](../run/run.html#filename=js_oper_mult "实例")  |
| /  | 除法  | x=y/2  | 2.5  | 5  | [实例](../run/run.html#filename=js_oper_div "实例")  |
| %  | 取模（余数） | x=y%2  | 1  | 5  | [实例](../run/run.html#filename=js_oper_mod "实例")  |
| ++  | 自增1  | x=++y  | 6  | 6  | [实例](../run/run.html#filename=js_oper_incr "实例")  |
| ++  | 自增2  | x=y++  | 5  | 6  | [实例](../run/run.html#filename=js_oper_incr2 "实例")  |
| --  | 自减1  | x=--y  | 4  | 4  | [实例](../run/run.html#filename=js_oper_decr "实例")  |
| --  | 自减2  | x=y--  | 5  | 4  | [实例](../run/run.html#filename=js_oper_decr2 "实例")  |

## JavaScript 赋值运算符

赋值运算符用于给 JavaScript 变量赋值。

给定 **x=10** 和 **y=5**，下面的表格解释了赋值运算符：

| 运算符  | 例子  | 等同于  | 运算结果  | 在线实例  |
| :------------ | :------------ | :------------ | :------------ | ------------ |
| =  | x=y  |    | x=5  | [实例](../run/run.html#filename=js_oper_equal "实例")  |
| +=  | x+=y  | x=x+y  | x=15  | [实例](../run/run.html#filename=js_oper_plusequal "实例")  |
| -=  | x-=y  | x=x-y  | x=5  | [实例](../run/run.html#filename=js_oper_minequal "实例")  |
| `*= ` |` x*=y`  | `x=x*y`  | x=50  | [实例](../run/run.html#filename=js_oper_multequal "实例")  |
| /=  | x/=y  | x=x/y  | x=2  | [实例](../run/run.html#filename=js_oper_divequal "实例")  |
| %=  | x%=y  | x=x%y  | x=0  | [实例](../run/run.html#filename=js_oper_modequal "实例")  |

## 用于字符串的 + 运算符

\+ 运算符用于把文本值或字符串变量加起来（连接起来）。

如需把两个或多个字符串变量连接起来，请使用 + 运算符。

实例
如需把两个或多个字符串变量连接起来，请使用 + 运算符：

<!--sec data-title="实例" data-filename="js_operators2" ces-->
```javascript
txt1="What a very";
txt2="nice day";
txt3=txt1+txt2;
```
txt3 运算结果如下:

```javascript
What a verynice day
```
<!--endsec-->

要想在两个字符串之间增加空格，需要把空格插入一个字符串之中：

<!--sec data-title="实例" data-filename="js_operators3" ces-->
```javascript
txt1="What a very ";
txt2="nice day";
txt3=txt1+txt2;
```
在以上语句执行后，变量 txt3包含的值是：

```javascript
What a very nice day
```
<!--endsec-->

或者把空格插入表达式中：:

<!--sec data-title="实例" data-filename="js_operators4" ces-->
```javascript
txt1="What a very";
txt2="nice day";
txt3=txt1+" "+txt2;
```
在以上语句执行后，变量txt3 包含的值是：

```javascript
What a very nice day
```
<!--endsec-->

## 对字符串和数字进行加法运算

两个数字相加，返回数字相加的和，如果数字与字符串相加，返回字符串，如下实例：

<!--sec data-title="实例" data-filename="js_operators5" ces-->
```javascript
x=5+5;
y="5"+5;
z="Hello"+5;
```
x,y, 和 z 输出结果为:

```javascript
10
55
Hello5
```
<!--endsec-->

**规则**:如果把数字与字符串相加，结果将成为字符串！