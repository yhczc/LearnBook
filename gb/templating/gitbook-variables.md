# 变量

以下是书籍解析和主题生成期间可用数据的参考。

## 全局变量

| 变量  | 描述  |
| :------------ | :------------ |
| `book`  | 书本信息+配置设置`book.json`。请参阅下文了解详情。  |
| `gitbook`  | GitBook的具体信息  |
| `page`  | 当前页面特定信息  |
| `file`  | 与当前页面特定信息相关联的文件  |
| `readme`  | 有关自述文件的信息  |
| `glossary`  | 有关词汇表的信息  |
| `summary`  | 有关目录的信息  |
| `languages`  | 多语言书籍的语言清单  |
| `output`  | 有关输出生成器的信息  |
| `config`  | 转储 `book.json`  |

## book变量

| 变量  | 描述  |
| :------------ | :------------ |
| `book.[CONFIGURATION_DATA]`  |  通过book变量可以获得`book.json`文件中所有的variables集合。 |
| `book.language `| 多语言书籍的当前语言  |

## GitBook变量

| 变量  | 变量  |
| :------------ | :------------ |
| `gitbook.time`  | 当前时间（运行gitbook命令时）。  |
| `gitbook.version`  | 用于生成书籍的GitBook版本  |

## 文件变量(file)

| 变量  | 描述  |
| :------------ | :------------ |
| `file.path`  | 原始页面的路径  |
| `file.mtime`  | 上次修改文件的 修改时间  |
| `file.type`  | 用于编译该文件解析器的名称（例如：markdown，asciidoc，等）  |

## 页面变量（page）

| 变量  | 描述  |
| :------------ | :------------ |
| `page.title`  | 页面标题  |
| `page.previous`  | 目录中的上一页（可以null）  |
| `page.next`  | 目录中的下一页（可以null）  |
| `page.dir`  | 文本方向，基于配置或从内容（`rtl`或`ltr`）中检测  |

## 目录变量（summary）

| 变量  | 描述  |
| :------------ | :------------ |
|` summary.parts`  | 目录中的部分列表  |

通过`summary.parts`变量可以访问整个目录(`SUMMARY.md`)：

`summary.parts[0].articles[0].title` 将返回第一篇文章的标题。

## 多语言书籍变量（languages）

| 变量  | 变量  |
| :------------ | :------------ |
| `languages.list`  | 本书的语言列表  |

语言定义为`{ id: 'en', title: 'English' }`。

## 输出变量（output）

| 变量  | 描述  |
| :------------ | :------------ |
| `output.name`  | 输出生成器的名称，可能值是`website`，`json`，`ebook`  |
| `output.format`  | 当output.name == "ebook"时，format定义了将要生成的电子书的格式，可能的值是`pdf`，`epub`或`mobi`  |

## 自述变量（readme）

| 变量  | 变量  |
| :------------ | :------------ |
| `readme.path`  | 书中自述文件的路径  |

## 词汇表变量（readme）

| 变量  | 描述  |
| :------------ | :------------ |
| `glossary.path`  | 书中词汇表的路径  |

