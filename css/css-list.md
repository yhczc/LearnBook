# CSS 列表

CSS列表属性作用如下：

- 设置不同的列表项标记为有序列表
- 设置不同的列表项标记为无序列表
- 设置列表项标记为图像

## 列表

在HTML中，有两种类型的列表：

- 无序列表 - 列表项标记用特殊图形（如小黑点、小方框等）
- 有序列表 - 列表项的标记有数字或字母

使用CSS，可以列出进一步的样式，并可用图像作列表项标记。

## 不同的列表项标记

list-style-type属性指定列表项标记的类型是：

<!--sec data-title="实例" data-filename="css_list-style-type_ex" ces-->
```css
ul.a {list-style-type: circle;}
ul.b {list-style-type: square;}
 
ol.c {list-style-type: upper-roman;}
ol.d {list-style-type: lower-alpha;}
```
<!--endsec-->

一些值是无序列表，以及有些是有序列表。

list-style-type属性用来定义列表所使用的项目符号的类型，可选值有 none | disc | circle | square | decimal | decimal-leading-zero | lower-alpha | upper-alpha | lower-roman | upper-roman，默认值为 disc。常用属性值如下：

| 属性值  | 属性值  |
| ------------ | ------------ |
| none  | 不使用任何项目符号  |
| disc  | 默认值，实心圆  |
| circle  | 空心圆  |
| square  | 实心矩形  |
| decimal  | 数字1、2、3、4、5  |
| decimal-leading-zero  | 以0打头的数字，01、02、03、04、05  |
| lower-alpha  | 小写英文字母，a、b、c、d、e  |
| upper-alpha  | 大写英文字母，A、B、C、D、E  |
| lower-roman  | 小写罗马数字，ⅰ、ⅱ、ⅲ、ⅳ、ⅴ  |
| upper-roman  | 大写罗马数字，Ⅰ、Ⅱ、Ⅲ、Ⅳ、Ⅴ  |

## 作为列表项标记的图像

要指定列表项标记的图像，使用列表样式图像属性：

<!--sec data-title="实例" data-filename="css_list-style-image" ces-->
```css
ul
{
    list-style-image: url('sqpurple.gif');
}
```
<!--endsec-->

上面的例子在所有浏览器中显示并不相同，IE和Opera显示图像标记比火狐，Chrome和Safari更高一点点。

如果你想在所有的浏览器放置同样的形象标志，就应使用浏览器兼容性解决方案，过程如下

## 浏览器兼容性解决方案

同样在所有的浏览器，下面的例子会显示的图像标记：

<!--sec data-title="实例" data-filename="css_list-style-image_crossbrow" ces-->
```css
ul
{
    list-style-type: none;
    padding: 0px;
    margin: 0px;
}
ul li
{
    background-image: url(sqpurple.gif);
    background-repeat: no-repeat;
    background-position: 0px 5px; 
    padding-left: 14px; 
}
```
<!--endsec-->

例子解释：

- ul:
 - 设置列表样式类型为没有删除列表项标记
 - 设置填充和边距0px（浏览器兼容性）
- ul中所有li:
 - 设置图像的URL，并设置它只显示一次（无重复）
 - 您需要的定位图像位置（左0px和上下5px）
- 用padding-left属性把文本置于列表中

## 列表 -简写属性

在单个属性中可以指定所有的列表属性。这就是所谓的简写属性。

为列表使用简写属性，列表样式属性设置如下：

<!--sec data-title="实例" data-filename="css_list-style-image_crossbrow" ces-->
```css
ul
{
    list-style: square url("sqpurple.gif");
}
```
<!--endsec-->

可以按顺序设置如下属性：

- list-style-type
- list-style-position (有关说明，请参见下面的CSS属性表)
- list-style-image

如果上述值丢失一个，其余仍在指定的顺序，就没关系。

## 更多实例

[所有不同的列表项标记](http://# "所有不同的列表项标记")

这个例子演示了所有不同的CSS列表项标记。

## 所有的CSS列表属性

| 属性  | 描述  |
| ------------ | ------------ |
| list-style  | 简写属性。用于把所有用于列表的属性设置于一个声明中  |
| list-style-image  | 将图象设置为列表项标志。  |
| list-style-position  | 设置列表中列表项标志的位置。  |
| list-style-type  | 设置列表项标志的类型。  |

