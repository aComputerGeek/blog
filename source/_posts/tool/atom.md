---
title: test1
date: 2017-12-11 12:35:24
tags: 工欲善必先利器
---


5.29
  atom    ctrl + shift + m  markdown预览
    markdown-preview-plus   增强显示
      支持预览实时渲染。(Ctrl + Shift + M)
      支持Latex公式。(Ctrl + Shift + X)
      先禁用markdown-preview。

    markdown-scroll-sync    同步滚动(对markdown-preview-plus 不生效)
    markdown-image-paste    图片粘贴 （文件目录生成图片） ctrl + v  mac下也是
    language-markdown       代码语法增强
    markdown-table-editor   表格编辑
    markdown-themeable-pdf、pdf-view   pdf导出
        从官网下载phantomjs二进制安装包：http://phantomjs.org/download.html
        解压下载的phantomjs-2.1.1-macosx.zip压缩文件。
        添加index.js文件到解压后的目录。
        将整个目录的内容拷贝到：~/.atom/packages/markdown-themeable-pdf/node_modules/phantomjs-prebuilt，注意目录phantomjs-2.1.1-macosx被重命名为phantomjs-prebuilt
        重启Atom，右键->Markdown to PDF即可，生成的pdf文件在Markdown文件同目录。

        其中index.js文件内容为：
        module.exports = {
          path : __dirname + '/bin/phantomjs'
        }
