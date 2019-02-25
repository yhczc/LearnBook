# 内置模板辅助

GitBook提供了一系列内置过滤器和块来帮助您编写模板。

## 过滤器

value|default(default, [boolean])如果值严格未定义，则返回default，否则返回value。如果boolean为true，则任何JavaScript falsy值都将返回default（false，“”等）

arr|sort(reverse, caseSens, attr) 使用JavaScript的arr.sort函数对arr进行排序。如果反向为真，则结果将反转。默认情况下，Sort不区分大小写，但将caseSens设置为true会使其区分大小写。如果传递attr，将比较每个项目的attr。

## 块

使用 Markdown 渲染 内容，如下简单示例：

```markdown
{% markdown %}Markdown string{% endmarkdown %}
```

使用 AsciiDoc 渲染 内容，如下简单示例：

```asciidoc 
{% asciidoc %}AsciiDoc string{% endasciidoc %} 
```

