# 模板

GitBook使用[Nunjucks模板语言](https://mozilla.github.io/nunjucks/ "Nunjucks模板语言")来处理页面和主题模板。

Nunjucks语法与**Jinja2**或**Liquid**非常相似。它的语法使用周围的大括号{ }来标记需要处理的内容。

## 变量

变量从模板上下文中查找值。如果您只想显示变量，则可以使用`{{ variable }}`语法。例如 ：

```twig
My name is {{ name }}, nice to meet you
```
这将从上下文中查找用户名并显示它。变量名称可以在其中包含查找属性的点，就像JavaScript一样。您还可以使用方括号语法。

```twig
{{ foo.bar }}
{{ foo["bar"] }}
```

如果未定义值，则不显示任何内容。如果foo未定义`{{ foo }}`，则以下所有内容均不输出：`{{ foo.bar }}`,` {{ foo.bar.baz }}`。

GitBook 从上下文中提供了一组[预定义变量](/templating/variables.html "预定义变量")。

## 过滤器

过滤器本质上是可以应用于变量的函数。它们使用管道运算符（`|`）调用，并且可以接受参数。

```twig
{{ foo | title }}
{{ foo | join(",") }}
{{ foo | replace("foo", "bar") | capitalize }}
```

第三个示例显示了如何链接过滤器。它将显示“Bar”，首先将“foo”替换为“bar”，然后将其大写。

## 标签

### if

`if`测试条件并允许您有选择地显示内容。它的行为与JavaScript的`if`行为完全相同。

```twig
{% if variable %}
  It is true
{% endif %}
```

如果定义了变量并且计算结果为true，则将显示“It is true”。否则，什么都不会。

您可以使用`elif`和指定备用条件`else`：

```twig
{% if hungry %}
  I am hungry
{% elif tired %}
  I am tired
{% else %}
  I am good!
{% endif %}
```

### for

for 迭代数组和字典。

```twig
# Chapters about GitBook

{% for article in glossary.terms['gitbook'].articles %}
* [{{ article.title }}]({{ article.path }})
{% endfor %}
```

### set

set 允许您创建/修改变量。

```twig
{% set softwareVersion = "1.0.0" %}

Current version is {{ softwareVersion }}.
[Download it](website.com/download/{{ softwareVersion }})
```
### include and block

`include` and `block`在"[内容引用](/templating/gitbook-conrefs.html "内容引用")"部分中详细说明。

### 转义
如果你想让GitBook忽略任何特殊的模板标签，你可以使用`raw`，它内部的任何内容都将以纯文本形式输出。

```twig
{% raw %}
  this will {{ not be processed }}
{% endraw %}
```

输出结果：

{% raw %}
  this will {{ not be processed }}
{% endraw %}
