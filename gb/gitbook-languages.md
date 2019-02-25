# 多语言支持

GitBook支持构建用多种语言编写的书籍。每种语言都应该是遵循普通GitBook格式的子目录，并且命名的文件`LANGS.md`应该存在于存储库的根目录中，格式如下：

```markdown
# Languages

* [English](en/)
* [French](fr/)
* [Español](es/)
```
## 每种语言的配置

当一本语言书(ex: en)有book.json时，其配置将扩展主配置。

唯一的例外是插件，插件是全局指定的，并且不能指定特定于语言的插件。
