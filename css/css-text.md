# CSS 文本格式

通过CSS的Text属性，你可以改变页面中文本的颜色、字符间距、对齐文本、装饰文本、对文本进行缩进等等，你可以观察下述的一段简单的应用了CSS文本格式的段落。

## 文本颜色

颜色属性被用来设置文字的颜色。

颜色是通过CSS最经常的指定：

- 十六进制值 - 如: ＃FF0000
- 一个RGB值 - 如: RGB(255,0,0)
- 颜色的名称 - 如: red

参阅 CSS 颜色值 查看完整的颜色值。

一个网页的背景颜色是指在主体内的选择：

<!--sec data-title="实例" data-filename="css_color" ces-->
```css
body {color:red;}/*指定body所有文本默认颜色*/
h1 {color:#00ff00;}/*指定h1标题文本颜色*/
h2 {color:rgb(255,0,0);}/*指定ex类段落文本颜色*/
```
<!--endsec-->

> [!TIP] 
>  对于W3C标准的CSS：如果你定义了颜色属性，你还必须定义背景色属性。

## 文本的对齐方式

文本排列属性是用来设置文本的水平对齐方式。

文本可居中或对齐到左或右,两端对齐.

当text-align设置为"justify"，每一行被展开为宽度相等，左，右外边距是对齐（如杂志和报纸）。

<!--sec data-title="实例" data-filename="css_text-align_all" ces-->
```css
h1 {text-align:center;}
p.date {text-align:right;}
p.main {text-align:justify;}
```
<!--endsec-->

## 文本修饰

text-decoration 属性用来设置或删除文本的装饰。

从设计的角度看 text-decoration属性主要是用来删除链接的下划线：

<!--sec data-title="实例" data-filename="css_text-decoration_link" ces-->
```css
a {text-decoration:none;}
```
<!--endsec-->

也可以这样装饰文字：

<!--sec data-title="实例" data-filename="css_text-decoration" ces-->
```css
h1 {text-decoration:overline;}
h2 {text-decoration:line-through;}
h3 {text-decoration:underline;}
```
<!--endsec-->

> [!TIP] 
>  我们不建议强调指出不是链接的文本，因为这常常混淆用户。

## 文本转换

文本转换属性是用来指定在一个文本中的大写和小写字母。

可用于所有字句变成大写或小写字母，或每个单词的首字母大写。

<!--sec data-title="实例" data-filename="css_text-transform" ces-->
```css
p.uppercase {text-transform:uppercase;}
p.lowercase {text-transform:lowercase;}
p.capitalize {text-transform:capitalize;}
```
<!--endsec-->

## 文本缩进

文本缩进属性是用来指定文本的第一行的缩进。

<!--sec data-title="实例" data-filename="css_text-indent" ces-->
```css
p {text-indent:50px;}
```
<!--endsec-->

## 更多实例

[指定字符之间的空间](http://# "指定字符之间的空间")

这个例子演示了如何增加或减少字符之间的空间。

[指定行与行之间的空间](http://# "指定行与行之间的空间")

这个例子演示了如何指定在一个段落中行之间的空间

[设置元素的文本方向](http://# "设置元素的文本方向")

这个例子演示了如何改变元素的文本方向。

[增加单词之间的空白空间](http://# "增加单词之间的空白空间")

这个例子演示了如何增加一个段落中的单词之间的空白空间。

[在元素内禁用文字环绕](http://# "在元素内禁用文字环绕")

这个例子演示了如何禁用一个元素内的文字环绕。

[垂直对齐图像](http://# "垂直对齐图像")

这个例子演示了如何设置文本的垂直对齐图像。

[添加文本阴影](http://# "添加文本阴影")

这个例子演示了如何设置文本阴影。

## 所有CSS文本属性。

| 属性  | 描述  |
| ------------ | ------------ |
| color  | 设置文本颜色  |
| direction  | 设置文本方向  |
| letter-spacing  | 设置字符间距  |
| line-height  | 设置行高  |
| text-align  | 对齐元素中的文本  |
| text-decoration  | 向文本添加修饰  |
| text-indent  | 缩进元素中文本的首行  |
| text-shadow  | 设置文本阴影  |
| text-transform  | 控制元素中的字母  |
| unicode-bidi  | 设置或返回文本是否被重写   |
| vertical-align  | 设置元素的垂直对齐  |
| white-space  | 设置元素中空白的处理方式  |
| word-spacing  | 设置字间距  |
