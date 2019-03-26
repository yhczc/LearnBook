# CSS 字体

CSS 字体属性定义文本的字体系列、大小、加粗、风格（如斜体）和变形（如小型大写字母）。

## CSS 字体系列

在 CSS 中，有两种不同类型的字体系列名称：

- 通用字体系列 - 拥有相似外观的字体系统组合（比如 "Serif" 或 "Monospace"）
- 特定字体系列 - 具体的字体系列（比如 "Times" 或 "Courier"）

CSS 定义了 5 种通用字体系列：

- Serif 字体
- Sans-serif 字体
- Monospace 字体
- Cursive 字体
- Fantasy 字体

如果需要了解更多有关字体系列的知识，请阅读 [CSS 字体系列](http://# "CSS 字体系列")。

## 指定字体系列

在CSS中，通过 font-family属性来指定文本所使用的字体系列。语法格式为：

```css
font-family: [<family-name> | <generic-family>] 
```

其中，family-name为特定字体系列的名称；generic-family为通用字体系列的名称。也就是说，font-family属性的值既可以是具体的字体系列的名称，也可以是通用字体系列的名称。

### 使用通用字体系列

如果你希望文档使用一种 sans-serif 字体，但是你并不关心是哪一种字体，以下就是一个合适的声明：

<!--sec data-title="实例" data-filename="css_font_family_generic" ces-->
```css
body {font-family: sans-serif;}
```
<!--endsec-->

这样用户代理就会从 sans-serif 字体系列中选择一个字体（如 Helvetica），并将其应用到 body 元素。因为有继承，这种字体选择还将应用到 body 元素中包含的所有元素，除非有一种更特定的选择器将其覆盖。

> [!TIP] 注意：虽然 font-family属性具有继承性，但有几个元素不会继承父元素的字体设置，其中有表单的 select、textarea 和input 元素。不过，可以强制它们继承父元素的字体设置。代码如下：

>```css
input, select, textarea {
 font-family: inherit;
}
```

### 指定字体系列

除了使用通用的字体系列，您还可以通过 font-family 属性设置更具体的字体。

下面的例子为所有 h1 元素设置了 Georgia 字体：

<!--sec data-title="实例" data-filename="css_font_family_specific" ces-->
```css
h1 {font-family: Georgia;}
```
<!--endsec-->

这样的规则同时会产生另外一个问题，如果用户代理上没有安装 Georgia 字体，就只能使用用户代理的默认字体来显示 h1 元素。

我们可以通过结合特定字体名和通用字体系列来解决这个问题：

<!--sec data-title="实例" data-filename="css_font_family_fallback_1" ces-->
```css
h1 {font-family: Georgia, serif;}
```
<!--endsec-->

如果读者没有安装 Georgia，但安装了 Times 字体（serif 字体系列中的一种字体），用户代理就可能对 h1 元素使用 Times。尽管 Times 与 Georgia 并不完全匹配，但至少足够接近。

因此，我们建议在所有 font-family 规则中都提供一个通用字体系列。这样就提供了一条后路，在用户代理无法提供与规则匹配的特定字体时，就可以选择一个候选字体。

如果您对字体非常熟悉，也可以为给定的元素指定一系列类似的字体。要做到这一点，需要把这些字体按照优先顺序排列，然后用逗号进行连接：

<!--sec data-title="实例" data-filename="css_font_family_fallback_2" ces-->
```css
p {font-family: Times, TimesNR, 'New Century Schoolbook',
     Georgia, 'New York', serif;}
```
<!--endsec-->

根据这个列表，用户代理会按所列的顺序查找这些字体。如果列出的所有字体都不可用，就会简单地选择一种可用的 serif 字体。

### 使用引号

您也许已经注意到了，上面的例子中使用了单引号。只有当字体名中有一个或多个空格（比如 New York），或者如果字体名包括 # 或 $ 之类的符号，才需要在 font-family 声明中加引号。

单引号或双引号都可以接受。但是，如果把一个 font-family 属性放在 HTML 的 style 属性中，则需要使用该属性本身未使用的那种引号：

<!--sec data-title="实例" data-filename="css_font_family_quote" ces-->
```css
<p style="font-family: Times, TimesNR, 'New Century Schoolbook', Georgia,
 'New York', serif;">...</p>
```
<!--endsec-->