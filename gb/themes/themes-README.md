# 主题

从版本3.0.0开始，GitBook可以轻松主题化。默认情况下，书籍使用主题[默认主题](https://github.com/GitbookIO/theme-default "默认主题")。

> **[warning] 警告**
>
> 自定义主题可能会阻止某些插件正常工作。

## 主题结构

主题是包含模板和资源的插件。覆盖任何单个模板是可选的，因为主题始终扩展默认主题。

| 文件夹/文件  | 描述  |
| ------------ | ------------ |
| `_layouts` | _layouts/ebook/page.html  |
|   `_layouts/website/page.html`  | 普通页面的模板 |
| `_layouts/ebook/page.html`  | 电子书生成期间正常页面的模板（PDF <ePub，Mobi）  |

## 扩展/自定义书中的主题

作者可以直接从他们的书籍来源扩展主题的模板（无需创建外部主题）。模板将首先在`_layouts`本书的文件夹中解析，然后在已安装的插件/主题中解析。

## 延伸而不是分叉

如果要将主题更改提供给多本书，而不是分支默认主题，可以使用[模板语法]/templating/ "模板语法")对其进行扩展：

```html
{% extends template.self %}

{% block body %}
    {{ super() }}
    ... This will be added to the "body" block
{% endblock %}
```

请查看API主题以获得更完整的示例。

## 发布主题

主题作为插件发布（[请参阅相关文档](/plugins/ "请参阅相关文档")），并带有`theme-`前缀。例如，主题`awesome`将从`theme-awesome`插件加载，然后从 `gitbook-plugin-theme-awesome` NPM包加载。
