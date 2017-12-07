---
title: hexo搭建博客
date: 2017-12-07 23:46:21
tags:
 - test
 - test2
updated: 	2017-12-07 23:50:00
comments: true
categories:
  - 一级分类
  - 二级分类
---

# Hexo简介

    Hexo 是一个快速、简洁且高效的博客框架。
    Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

**相关**
* [Hexo官方文档](https://hexo.io/zh-cn/docs/index.html)
* [next主题官网](http://theme-next.iissnan.com/getting-started.html)

## 安装使用

**前提**
* Node.js
* Git

## 配置项说明


## 命令

#### init
新建一个项目。默认在当前目录建立
```
$ hexo init [folder]
```

#### new
新建一篇文章
```
$ hexo new [layout] <title>
```
新建一篇文章。如果没有设置 layout 的话，默认使用 `_config.yml` 中的 `default_layout` 参数代替。如果标题包含空格的话，请使用引号括起来。

#### generate
生成静态文件
```
$ hexo generate
```
可简写为
```
$ hexo g
```
**hexo generate参数**

| 选项 | 描述 |
| :------------- | :------------- |
|-d, --deloy|文件生成后立即部署网站|
|-w, --watch|监视文件变动|

#### publish
发表草稿
```
$ hexo publish [layout] <filename>
```

#### Server
启动服务器，默认地址为 `http://localhost:4000`
```
$ hexo server
```

| 选项 | 描述 |
| :------------- | :------------- |
| -p, --port | 重设端口 |
| -s, --static | 只使用静态文件 |
| -l, --log | 启动日志记录，使用覆盖记录格式 |

#### deploy
部署项目
```
$ hexo deploy
```
可简写为
```
hexo d
```

| 选项 | 描述 |
| :------------- | :------------- |
| -g, --generate | 部署之前预先生成静态文件 |

#### render
渲染文件
```
$ hexo render <file1> [file2] …………
```

| 选项 | 描述 |
| :------------- | :------------- |
| -o, --output | 设置输出路径 |

#### migrate
迁移
```
hexo migrate <type>
```

#### clean
```
$ hexo clean
```
清除缓存文件 (db.json) 和已生成的静态文件 (public)。
在某些情况（尤其是更换主题后），如果发现您对站点的更改无论如何也不生效，您可能需要运行该命令。

#### list
列出网站资料
```
$ hexo list <type>
```
显示Hexo版本
```
hexo versiong
```

### 选项

#### 安全模式
```
$ hexo --safe
```
在安全模式下，不会载入插件和脚本。当您在安装新插件遭遇问题时，可以尝试以安全模式重新执行

#### 调试模式
```
$ hexo --debug
```
在终端中显示调试信息并记录到 debug.log。当您碰到问题时，可以尝试用调试模式重新执行一次，并 提交调试信息到 GitHub。

#### 简介模式
```
$ hexo --silent
```
隐藏终端信息

#### 自定义配置文件的路径
```
$ hexo --config custom.yml
```
自定义配置文件的路径，执行后将不再使用 `_config.yml`。

**显示草稿**
```
$ hexo --draft
```
显示 `source/_drafts` 文件夹中的草稿文章。

**自定义CWD**
```
$ hexo --cwd /path/to/cwd
```
自定义当前工作目录（Current working directory）的路径。

# 线上配置

# 功能增强

# 美化设置
