# 在 NotePad++ 中使用 MarkDown

需要安装两个插件，语法高亮部分及NppMarkdown，NotePad++安装32bit版

## 语法高亮

[下载地址](https://github.com/Edditoria/markdown_npp) ，项目中有四种MarkDown语法高亮皮肤。

选择自己的高亮方案导入NotePad++中，导入方法：**语言 -> 自定义语言格式 -> 导入** 。导入完成后在`语言` 菜单项下部会出现 `MarkDown`


## MarkDown 预览
安装 NppMarkDown预览插件，项目地址[NppMarkdown](https://github.com/gclxry/NppMarkdown) ，编译后的插件[百度网盘](http://pan.baidu.com/s/1c08pOjQ) 

将下载的NppMarkdown.dll 插件拷贝至 NotePad 安装目录下的 `plugins` 中即可。

安装后，在NotePad++中菜单 `插件` 下会出现**NppMarkDown**选项。

## 另类预览方式

该方式是通过**pandoc**将MarkDown文件转换为html文件，然后使用**Preview HTML**插件来完成预览。

需要安装**PanDoc**及**Preview HTML**插件，然后

1、设置转换规则

```
; Content of Filter.ini file
[Markdown]
Extension=.md
Command=pandoc --template=tpl.html5 --highlight-style=tango --mathjax="http://cdn.bootcss.com/mathjax/2.5.3/MathJax.js?config=TeX-AMS-MML_HTMLorMML" "%1"
```

2、设置刷新间隔

```
[Autorefresh]
Interval=0
```

```plantuml
@startuml
scale 3
Amber -> Hsing : test
@enduml
```
