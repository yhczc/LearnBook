# 插件

插件是扩展 GitBook 功能（电子书和网站）的最佳方式。有很多插件可以做很多事情：带来数学公式显示支持，使用 Google Analytic 跟踪访问等。

## 如何找到插件？

- 可以在[ GitBook 插件库](https://plugins.gitbook.com/ " GitBook 插件库")上轻松搜索插件。
- 也可以在 [NPM](https://www.npmjs.com/ "NPM") 包管理器中搜索插件，以`gitbook-plugin-`开头的名称为 GitBook 插件，以`gitbook-plugin-theme-`开头的名称为 GitBook 主题插件。

## 如何安装插件？

找到要安装的插件后，需要将其添加到`book.json`：

```json
{
   "plugins": ["myPlugin", "anotherPlugin"],
    "pluginsConfig": {
      "myPlugin": {
            "message": "Hello World"
        }
    }
}
```

您还可以使用`“myPlugin@0.3.1”`指定一个特定的版本，表示获取`0.3.1`版本的插件。默认情况下，GitBook 将获取最新版本的插件。

`pluginsConfig`用于存储插件一些特定配置信息。您必须参考插件本身的文档以获取有关可用选项的详细信息。

## legacy.gitbook.com

插件会自动安装在legacy.gitbook.com上。如是在本地部署，运行`gitbook install`命令以安装配置中的所有插件。


