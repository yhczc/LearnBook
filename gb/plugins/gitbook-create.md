## 创建并发布插件

GitBook插件是在[NPM](https://www.npmjs.com "NPM")上发布的遵循定义约定的节点包。

## 文件结构

### package.json

`package.json`是用于描述**Node.js模块**的清单格式。GitBook插件构建在Node模块之上。它声明了在GitBook中运行插件所需的依赖项，版本，所有权和其他信息。本文档详细描述了架构。

插件清单package.json还可以包含有关所需配置的详细信息。配置模式`gitbook`在`package.json`（此字段遵循[JSON-Schema](http://json-schema.org/ "JSON-Schema")准则）的字段中定义：

```json
{
    "name": "gitbook-plugin-mytest",
    "version": "0.0.1",
    "description": "This is my first GitBook plugin",
    "engines": {
        "gitbook": ">1.x.x"
    },
    "gitbook": {
        "properties": {
            "myConfigKey": {
                "type": "string",
                "default": "it's the default value",
                "description": "It defines my awesome config!"
            }
        }
    }
}
```

您可以`package.json`从[NPM文档](https://docs.npmjs.com/files/package.json "NPM文档")中了解更多信息。

该包的名称必须以`gitbook-plugin-`开头且`package.json`内容应该包含`gitbook`选项参数信息。

### index.js

这 index.js 是插件运行时的主要入口点：

```javascript
module.exports = {
    // Map of hooks
    hooks: {},

    // Map of new blocks
    blocks: {},

    // Map of new filters
    filters: {}
};
```

## 发布您的插件

GitBook 插件可以在[NPM](https://www.npmjs.com/ "NPM")上发布。

要发布新插件，您需要在[npmjs.com](https://www.npmjs.com "npmjs.com")上创建一个帐户，然后从命令行发布它：

```shell
$ npm publish
```

## 私人插件

私有插件可以在 GitHub 上托管，并使用 `git` url 包含：

```json
{
    "plugins": [
        "myplugin@git+https://github.com/MyCompany/mygitbookplugin.git#1.0.0"
    ]
}
```
