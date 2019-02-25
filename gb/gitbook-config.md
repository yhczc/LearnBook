# 配置
GitBook允许您使用灵活的配置自定义您的书。这些选项在`book.json`文件中指定。对于不熟悉JSON语法的作者，您可以使用[JSON](https://www.json.cn/# "JSON")等工具验证语法。

## 常规设置

| 变量  | 描述  |
| :------------ | :------------ |
| `root`  | 包含所有书籍文件的根文件夹的路径，除外 `book.json`|
| `structure`  | 指定自述文件，摘要，词汇表等的路径。请参阅结构段落。  |
| `title`  | 您的图书的标题，默认值是从README中提取的。在legacy.gitbook.com上，此字段已预先填写。  |
| `description`  | 您的书的描述，默认值是从README中提取的。在legacy.gitbook.com上，此字段已预先填写。  |
| `author`  | 作者姓名。在legacy.gitbook.com上，此字段已预先填写。  |
| `isbn`  |  这本书的`ISBN` |
| `language`  | 本书语言的[ISO代码](https://baike.baidu.com/item/ISO%203166-1/5269555 "ISO代码")，默认值为en  |
| `direction`  | 文字的方向。可以是`rtl`或者`ltr`，默认值取决于值`language`  |
| `gitbook`  | 应该使用的GitBook版本。使用[SemVer规范](https://semver.org/lang/zh-CN/ "SemVer规范")并接受类似的条件">= 3.0.0"  |

## 插件

插件及其配置在`book.json`。中指定。有关更多详细信息，请参阅插件部分。

从版本3.0.0开始，GitBook可以使用主题。有关详细信息，请参阅主题部分。

| 变量  | 描述  |
| :------------ | :------------ |
| `plugins`  | 要加载的插件列表  |
| `pluginsConfig`  | 插件配置  |

## 结构体

除了`root`变量之外，您还可以告诉Gitbook自述文件，摘要，词汇表，语言的文件名称（而不是使用默认名称`README.md`）。这些文件必须位于您书籍的根目录（或每本语言书籍的根目录）。`dir/MY_README.md`不接受这样的路径。

| 变量  | 描述  |
| :------------ | :------------ |
| `structure.readme`  | 自述文件名（默认为`README.md`）  |
| `structure.summary`  | 摘要文件名（默认为`SUMMARY.md`）  |
| `structure.glossary`  | 词汇表文件名（默认为`GLOSSARY.md`）  |
| `structure.languages`  | 语言文件名（默认为`LANGS.md`）  |

## PDF选项

PDF输出可以使用以下选项中的一组选项进行自定义`book.json`：

| 变量  | 描述  |
| :------------ | :------------ |
| `pdf.pageNumbers`  | 将页码添加到每个页面的底部（默认为`true`）  |
| `pdf.fontSize`  | 基本字体大小（默认为`12`）  |
| `pdf.fontFamily`  | 基本字体系列（默认为`Arial`）  |
| `pdf.paperSize`  | 纸张尺寸，选项是`'a0', 'a1', 'a2', 'a3', 'a4', 'a5', 'a6', 'b0', 'b1', 'b2', 'b3', 'b4', 'b5', 'b6', 'legal', 'letter'`（默认是`a4`）  |
| `pdf.margin.top`  | 上边距（默认为`56`） |
| `pdf.margin.bottom`  | 底部保证金（默认为`56`）  |
| `pdf.margin.right`  | 右边距（默认为`62`）  |
| `pdf.margin.left`  | 左边距（默认为`62`）  |

