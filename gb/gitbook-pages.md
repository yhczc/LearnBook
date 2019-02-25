# 页面和摘要

## 摘要

GitBook使用一个`SUMMARY.md`文件来定义本书的章节和子章节的结构。该SUMMARY.md文件用于生成图书的目录。

格式`SUMMARY.md`只是一个链接列表。链接的标题用作章节的标题，链接的目标是该章节文件的路径。

将嵌套列表添加到父章节将创建子章节。

### 简单的例子

```markdown
# Summary

* [Part I](part1/README.md)
    * [Writing is nice](part1/writing.md)
    * [GitBook is nice](part1/gitbook.md)
* [Part II](part2/README.md)
    * [We love feedback](part2/feedback_please.md)
    * [Better tools for authors](part2/better_tools.md)
```

每章都有一个专用页面（`part#/README.md`），并分为子章节。

### 锚

目录中的章节可以使用锚点指向文件的特定部分。

```markdown
# Summary

### Part I

* [Part I](part1/README.md)
    * [Writing is nice](part1/README.md#writing)
    * [GitBook is nice](part1/README.md#gitbook)
* [Part II](part2/README.md)
    * [We love feedback](part2/README.md#feedback)
    * [Better tools for authors](part2/README.md#tools)
```

### 部分

目录可以分为由标题或水平线分隔的部分：

```markdown
# Summary

### Part I

* [Writing is nice](part1/writing.md)
* [GitBook is nice](part1/gitbook.md)

### Part II

* [We love feedback](part2/feedback_please.md)
* [Better tools for authors](part2/better_tools.md)

----

* [Last part without title](part3/title.md)
```

部件只是章节组，没有专用页面，但根据主题，它将显示在导航中。

## 网页

### Markdown语法

GitBook的大多数文件默认使用Markdown语法。GitBook从中推断出你网页的结构。使用的语法类似于[GitHub Flavored Markdown语法](https://guides.github.com/features/mastering-markdown/ "GitHub Flavored Markdown语法")。也可以选择[AsciiDoc](https://asciidoctor.org/docs/asciidoc-syntax-quick-reference/ "AsciiDoc")语法。

#### 章文件的示例

```markdown
# Title of the chapter

This is a great introduction.

## Section 1

Markdown will dictates _most_ of your **book's structure**

## Section 2

...
```

### 前方问题

页面可以包含可选的前端内容。它可用于定义页面的描述。前面的问题必须是文件中的第一件事，并且必须采用在三条虚线之间设置的有效YAML的形式。这是一个基本的例子：

```markdown
---
description: This is a short description of my page
---

# The content of my page
...
```

前面的事情可以定义您自己的变量，它们将被添加到页面变量中，以便您可以在模板中使用它们。
