# 内容引用

内容引用（conref）是一种方便的机制，可以重用其他文件或书籍中的内容。

## 导入本地文件
使用`include`标记可以轻松导入其他文件的内容：

```twig
{% include "./test.md" %}
```
## 从另一本书导入文件

GitBook也可以使用`git`解析包含路径：

```twig
{% include "git+https://github.com/GitbookIO/documentation.git/README.md#0.0.1" %}
```
git url的格式是：

```twig
git+https://user@hostname/owner/project.git/file#commit-ish
```

真正的git url部分应该完成`.git`，导入的文件名是`.git`在url的片段之后提取的。

`commit-ish`可以是任何标签，或分支可以作为参数被供给`git checkout`。默认是`master`。

## 继承

模板继承是一种使重用模板变得容易的方法。编写模板时，您可以定义子模板可以覆盖的“块”。继承链可以随你所愿。

block定义模板上的一个部分并用名称标识它。基本模板可以指定块，子模板可以使用新内容覆盖它们。

```twig
{% extends "./mypage.md" %}

{% block pageContent %}
# This is my page content
{% endblock %}
```

在文件中`mypage.md`，您应指定可以扩展的块：

```twig
{% block pageContent %}
This is the default content
{% endblock %}

# License

{% include "./LICENSE" %}
```
