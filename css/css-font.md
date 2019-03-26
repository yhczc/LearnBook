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

## 字体风格

font-style 属性最常用于规定斜体文本。

该属性有三个值：

- normal - 文本正常显示
- italic - 文本斜体显示
- oblique - 文本倾斜显示

<!--sec data-title="实例" data-filename="css_font-style" ces-->
```css
p.normal {font-style:normal;}
p.italic {font-style:italic;}
p.oblique {font-style:oblique;}
```
<!--endsec-->

### italic 和 oblique 的区别

font-style 非常简单：用于在 normal 文本、italic 文本和 oblique 文本之间选择。唯一有点复杂的是明确 italic 文本和 oblique 文本之间的差别。

斜体（italic）是一种简单的字体风格，对每个字母的结构有一些小改动，来反映变化的外观。与此不同，倾斜（oblique）文本则是正常竖直文本的一个倾斜版本。

通常情况下，italic 和 oblique 文本在 web 浏览器中看上去完全一样。

## 字体变形

有时候，希望一篇文章中的英文单词或英文字母，无论是小写还是大写，统一变成大写，就可以使用 font-variant属性实现。

font-variant属性用来使英文字母变为小型大写字母，可选值有 normal | small-caps，默认值为 normal。normal 为正常的字体；small-caps 让字母变成小型大写字母，这意味着所有的小写字母均会被转换为大写，但字体更小。

<!--sec data-title="实例" data-filename="css_font-variant" ces-->
```css
.normal {
 font-variant: normal;
}
.small-caps {
 font-variant: small-caps;
}
```
<!--endsec-->

> [!TIP] font-variant属性只把段落中的小写字母变为大写，并缩小显示，而段落中的大写字母依然保持原样，没有进行转换。这样一来，转换出来的大写字母，比实际的大写字母尺寸要小，显得不太协调。所以，在转换对象中，建议不要包含大写字母。

## 字体大小

在CSS中，通过 [font-size属性](http://# "font-size属性")来设置元素中所包含文本的字体大小。如果一个元素没有显式定义font-size属性，则会自动继承父元素的 font-size属性的计算结果。

定义 font-size 时，可以使用预定义关键字、绝对尺寸、相对尺寸。

### 预定义关键字

预定义关键字有 xx-small、x-small、small、medium、large、x-large、xx-large，尺寸按顺序依次增大，类似于衣服的尺寸。

使用预定义关键字有两大缺陷：一是只有 7 种选择，可选择范围太小；二是跟衣服的尺寸一样，不同厂商对每个关键字对应的字体大小的精确值可能各不不同，导致在不同浏览器下，文本的大小可能不同。因此，不推荐使用预定义关键字来定义字体的大小。

### 绝对尺寸

绝对尺寸有px（像素）、pt（点，1pt 相当于 1/72in）、in（英寸）、cm（厘米）、mm（毫米）等。

<!--sec data-title="实例" data-filename="css_font-size_absolutely" ces-->
```css
.px {
 font-size: 14px;
}
.pt {
 font-size: 10pt;
}
.in {
 font-size: .15in;
}
.cm {
 font-size: .4cm;
}
.mm {
 font-size: 4mm;
}
```
<!--endsec-->

上述代码定义了 5 种字体大小，都使用绝对单位。使用绝对长度单位后，在固定分辨率的显示器下，显示出来的都是固定大小。

如果以 px 为单位设置字体大小，使用IE浏览器的用户，就不能在浏览器上通过设置“文字大小”来对文本进行放大或缩小。如果文本太小，就会影响阅读，使用户体验大打折扣。

### 相对尺寸

相对尺寸有 em、%、rem，它们都是相对于某个参考基准的字体大小，来计算当前字体的大小，只是参考基准不同而已。

em 的参考基准是父元素。那么，如何计算要指定的 em 值呢？实际上，1em 总是等于父元素 font-size属性的值，这就是 em 的工作原理。据此，可以通过以下公式来确定百分比的值：

**目标元素的字体大小 / 父元素的字体大小 = 值**

因此，在使用 em 定义字体大小时，最好在 html 或 body 元素上建立一个基准。假设在 body 中设置的基准大小为 12px：

```css
body {
 font-size: 12px;
}
```

如果希望 body 中所有段落的字体大小为 18px，根据上述公式：

**18 / 12 = 1. 5**

因此，只需将将段落的 font-size 设置为 1.5em 就可以了，这条规则就表示段落文本的字体大小为父元素文本大小的1.5 倍：

<!--sec data-title="实例" data-filename="css_font-size_relative1" ces-->
```css
body p {
 font-size: 1.5em;
}
```
<!--endsec-->

% 的参考基准也是父元素，100% 也总是等于父元素 font-size属性的值，即 1em 就等于 100%。也就是说，在用 % 定义字体大小时，只需将 em 的值换算成相应的百分数即可。因此，以下两条声明会得到相同的结果（假设两个段落具有相同的父元素）：

<!--sec data-title="实例" data-filename="css_font-size_relative2" ces-->
```css
p.one {
 font-size: 1.5em;
}
p.two {
 font-size: 150%;
}
```
<!--endsec-->

需要注意的是，尽管 font-size 是可以继承的，但在使用 % 和 em 定义字体大小时，子元素继承的是计算结果的值，而不是 % 和 em 的数字。并且，% 和 em 还可以累积。考虑以下代码：

<!--sec data-title="实例" data-filename="css_font-size_relative3" ces-->
 ```css
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"> 
<title>马桶教程(gitmt.com)</title> 
<style>
p {
 font-size: 12px;
}
em {
 font-size: 200%;
}
strong {
 font-size: 200%;
}
</style>
</head>
<body>
<p>12px <em> 200% <strong> 200% </strong></em></p>
</body>
</html>
```
<!--endsec-->

上述代码中，p 为父元素，em 为 p 的子元素，strong 为 em 的子元素。em 元素的基准是 p 元素，而 strong 元素的基准是 em 元素。计算结果如下：

**em：12 × 200% = 24px**

**strong：24 × 200% = 48px**


在这种多层嵌套的情况下，如果某一个计算结果不是整数，浏览器可能就会取整，子元素再继承取整后的值。如果嵌套很深，下层的字体大小就越来越偏离实际计算值。并且，由于参考基准总是随着元素发生变化，嵌套越深，计算起来也就越困难。

鉴于此，CSS3中新增的一个相对单位 rem（root em的简称），它总是以文档的根元素（即 html 元素）为参考基准，来设置其它元素的字体大小，即 1rem 相当于 html 元素 font-size属性的值。考虑以下代码：

```css
html {
 font-size: 10px;
}
strong {
 font-size: 1.4rem;
}
```

上述声明中，strong 元素的字体大小将是 html 字体大小的1.4倍，则计算得到 strong 元素的字体大小就是1.4 × 10px = 14px。

这样一来，无论嵌套多少层，参考基准始终不变，计算字体大小就变得容易多了。不过，需要注意的是，rem 是CSS3新增的一个相对单位，IE9 以下版本的老浏览器却不支持它，这也是很多编程人员尚未使用 rem 的原因。

在定义字体大小时，笔者建议在 html 元素中定义绝大多数元素所需要的字体大小，并让所有子元素继承 html 的字体大小。如果某个子元素需要要改变字体大小，则使用相对尺寸 em 或 % 或 rem 重新定义。

这样做的好处是，一方面，绝大多数元素都不必定义字体大小，减少不必要的定义；另一方面，如果完成所有的文字排版后，又要统一调整页面文字大小，就可以只修改 html 中的字体大小，其它所有文字的字体大小会自动变化，修改起来就很容易。

> [!TIP]在某些特殊场景下，需要把 font-size 的值设置为0，来隐藏某些文本。但是，在IE6和IE7中，font-size: 0 的文本却变成了小黑点，并没有完全隐藏。

> 解决这个问题的最简单办法，就是在 font-size: 0 的同时，把 text-indent 属性设置为一个很大的负值，让这些文本显示在屏幕之外，自然就被隐藏起来。