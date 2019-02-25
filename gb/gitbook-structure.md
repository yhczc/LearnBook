##  目录结构

GitBook使用简单的目录结构。摘要中列出的所有Markdown / Asciidoc文件将转换为HTML。多语言书籍的结构略有不同。

一个基本的GitBook通常看起来像这样：

```bash
.
├── book.json
├── README.md
├── SUMMARY.md
├── chapter-1/
|   ├── README.md
|   └── something.md
└── chapter-2/
    ├── README.md
    └── something.md
```

概述每个方面的作用：

| 文件  | 描述  |
| :------------ | :------------ |
| book.json  | 存储配置数据（**可选**）  |
| README.md  | 您的书的前言/介绍（**必填**)  |
| SUMMARY.md  | 目录（参见页数）（**可选**）  |
| GLOSSARY.md  | 词典/注释术语列表（见术语表）（**可选**)  |

## 静态文件和图像

静态文件是未列在的文件`SUMMARY.md`。除非被忽略，否则所有静态文件都将复制到输出中。

## 忽略文件和文件夹

GitBook将读取`.gitignore`，`.bookignore`以及`.ignore`文件以获得文件和文件夹跳过列表。这些文件中的格式遵循以下相同的约定`.gitignore`：

```
# 这是一行注释

#  忽略 test.md
test.md

# 忽略目录“bin”中的所有内容
bin/*
```

## 项目与子目录集成

对于软件项目，您可以使用子目录（如`docs/`）来存储项目文档的书籍。您可以配置`root`选项以指示GitBook可以找到书籍文件的文件夹：

```
.
├── book.json
└── docs/
    ├── README.md
    └── SUMMARY.md
```

随着`book.json`含：

```
{
    "root": "./docs"
}
```
