# vscode

## 安装组件

1.ESLint

最初是由Nicholas C. Zakas 于2013年6月创建的开源项目。它的目标是提供一个插件化的javascript代码检测工具。

- 安装

启动 vscode，在左侧菜单中点击`扩展`菜单（快捷键 Ctrl + Shift + x）;

![](./img/vscode-01.png)

在扩展面板中搜索 `ESLint`，并点击安装。如果当前编辑器已安装，请略过；

2.Prettier

一个代码格式化工具，它可以支持 `JS/JSX/TS/Flow/JSON/CSS/LESS` 等文件格式。

- 安装

在扩展面板中搜索 `Prettier`，并点击安装。如果当前编辑器已安装，请略过；

3.Vetur

vscode 中支持 vue 的工具。

- 安装

在扩展面板中搜索 `Vetur`，并点击安装。如果当前编辑器已安装，请略过；


## 相关配置

vscode 提供了两种设置方式： 
- 用户设置： 这种方式进行的设置，会应用于该用户打开的所有工程； 
- 工作空间设置：工作空间是指使用 vscode 打开的某个文件夹，在该文件夹下会创建一个名为 `.vscode` 的隐藏文件夹，里面包含着**仅适用于当前目录的** vscode 的设置。工作空间的设置会覆盖用户的设置。

为保证项目规范统一，我们更改用户默认设置，打开设置面板方式如下：

- 点击 vscode 的`文件(File)` > `首选项(Preferred item)` > `设置(Setting)`，可以打开设置面板； 
- 在 vscode 中使用 `Ctrl + Shift + P` 打开命令面板，输入 `Preferences: Open User Settings`。

![](./img/vscode-02.png)

点击红色框标记的`打开配置json`，并在右侧`用户设置`添加如下配置（配置定期更新）：

```json
{
    // 常规设置
    "files.autoSave": "off",
    "window.zoomLevel": 0,
    "files.associations": {
      "*.tpl": "html",  // tpl 按照 html 格式支持
      "*.css": "less"  // css 支持 less 语法
    },
    "editor.fontSize": 12,
    "editor.multiCursorModifier": "ctrlCmd",
    "editor.detectIndentation": false,
    "editor.tabSize": 2,
    "terminal.integrated.fontSize": 12,
    "workbench.colorTheme": "Solarized Light",
    "editor.wordWrap": "wordWrapColumn",
    "editor.wordWrapColumn": 120,
    "css.lint.compatibleVendorPrefixes": "error",
    "css.lint.duplicateProperties": "error",
    "css.lint.emptyRules": "error",
    "css.lint.fontFaceProperties": "error",
    "css.lint.hexColorLength": "error",
    "css.lint.idSelector": "error",
    "css.lint.ieHack": "error",
    "css.lint.unknownProperties": "error",
    "css.lint.zeroUnits": "error",
    "css.validate": true,
    "less.lint.argumentsInColorFunction": "error",
    "less.lint.duplicateProperties": "error",
    "less.lint.emptyRules": "error",
    "less.lint.fontFaceProperties": "error",
    "less.lint.idSelector": "error",
    "less.lint.ieHack": "error",
    "less.lint.important": "error",
    "less.lint.universalSelector": "error",
    "less.lint.unknownProperties": "warning",
    "less.lint.zeroUnits": "error",
    "less.validate": true,
    "eslint.autoFixOnSave": true,
    "eslint.validate": [
      "javascript",
      "javascriptreact",
      {
        "language": "vue",
        "autoFix": true
      }
    ],

    "vetur.format.defaultFormatter.html": "js-beautify-html",
    "vetur.format.defaultFormatterOptions": {
      "js-beautify-html": {
        // Wrap attributes to new lines [auto|force|force-aligned|force-expand-multiline] ["auto"]
        "wrap_attributes": "force-expand-multiline"
      }
    },
    "prettier.singleQuote": true,
    "javascript.updateImportsOnFileMove.enabled": "always"
}
```

