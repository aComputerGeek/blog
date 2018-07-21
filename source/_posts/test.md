cd ---
title: test
date: 2017-12-07 23:46:21
tags:
---


npm-check检查更新
```
npm install -g npm-check
npm-check
```
npm-upgrade更新
```
npm install -g npm-upgrade
npm-upgrade
```

更新全局包：
```
npm update <name> -g
```
更新生产环境依赖包：
```
npm update <name> --save
```
更新开发环境依赖包：
```
npm update <name> --save-dev
```

```
// php函数，打印格式直接可以赋值
var_export
```

```
  // 打印sql语句

  \DB::connection()->enableQueryLog();

  数据库操作

  $sql = \DB::connection()->getQueryLog();
  \DB::connection()->disableQueryLog();
```

```
lumen
composer require symfony/var-dumper

Chrome 6.2 以上版本使用 dump () 或者 dd () 时,network Preview 无法渲染问题

当响应的状态码为400 or 500系列时可以使Preview渲染

// 修改响应码 为 400 或 500
http_response_code(500);
dd(request());

// 或者将 下面代码填到 live templates中， 或者添加一个 helperfunction
function ddd(...$args){
    http_response_code(500);
    call_user_func_array('dd', $args);
}
```

```
// 程序员的命令行搜索工具

### grep
// 如果你只想在PHP文件中找到一个短语并输出行号：
$ grep -RHn --include \*.php Controller .

// 搜索历史命令
$ history | grep 'php artisan'
  284  php artisan route:list
$ !284

查看占用端口进程， kill掉进程
lsof -i :端口号
kill -9 进程id
```

```
// 查看容器信息  并塞选 IPAddress 信息
docker inspect laravel_nginx_1 | grep "IPAddress"
```

```
// composer 忽略php版本
composer install --ignore-platform-reqs
```

图表第三方插件 hcharts：
https://www.hcharts.cn/

资源共享：
http://www.zygx8.com/forum-78-2.html

hexo官网：
https://hexo.io/zh-cn/docs/themes.html

hexo next皮肤官网
http://theme-next.iissnan.com/

关于配置hexo的博客
http://blog.csdn.net/sunshine940326/article/details/69933696

蚂蚁金服数据可视化
https://antv.alipay.com/zh-cn/index.html

墨者学院可视化
https://antv.alipay.com/zh-cn/vis/blog/index.html

easy mock 数据接口测试
https://www.easy-mock.com

```
// 隐藏当前工作
git stash

// 查看已存在的更改列表
git stash list

git status -s

// 将隐藏的工作返回到当前工作目录
git stash pop
```

```
https://www.elastic.co/
```


```
laravel 队列
https://www.lijinma.com/blog/2017/01/31/laravel-queue/

注意：
Redis 里面一个任务默认最多执行60秒，如果一个任务60秒没有执行完毕，会继续放回到队列中，循环执行
```

```
php 代码规范， 规范不对 不能提交
https://laravel-china.org/articles/13006/recommend-a-phpcs-plug-in-to-standardize-laravel-code-specification-from-local-code-to-version-control
```


```
批量入库时报错：prepared statement contains too many placeholders
原因：占位符的个数大于mysql对占位符的最高限制65535。
  条数 * 字段数
```

```
laravel  App\Exceptions\Handler::render  方法可以自定义错误返回信息 有时间仔细看下文档，读laravel
```

```
// 内网穿透
https://ngrok.com/docs
// wepy
https://tencent.github.io/wepy/
// 美团开源 mpvue vue转小程序
https://github.com/Meituan-Dianping/mpvue
// 小程序版weiui
https://github.com/weui/weui-wxss
// laravel包
jedrzej/searchable
```

```
// 自动化持续集成和部署
https://github.com/Piplin/Piplin
```

```
中文社区
掘金 推酷 segment v2ex
```

```
// 代理网站
https://free-ss.site/
http://webosss.com/tool/socket
https://blog.csdn.net/lihuaichen/article/details/70340039

digitalocean  搬瓦工
```

```
// mac软件下载
http://xclient.info/
// 玩转苹果-苹果改变世界！
http://www.ifunmac.com/
```

```
// 数据库重复判断
select client_guid,level,type,stage,count(*) from data_achievements_record group by client_guid,level,type,stage having count(*) > 1
```

```
// 整理好的各种学习资源的 github
https://github.com/EbookFoundation/free-programming-books/blob/master/free-programming-books-zh.md
// zsh 增强shell
https://github.com/robbyrussell/oh-my-zsh
// github 使用技巧
https://github.com/tiimgreen/github-cheat-sheet/
// 面试资料
https://github.com/francistao/LearningNotes
```


```
vue 中 慎用 scoped
https://segmentfault.com/a/1190000012184604?utm_source=tuicool&utm_medium=referral
```

```
laradock 中遇到时间不同步问题， docker-composer down / up 不能生效，
重启电脑后解决。
没有试过 重启docker
```


```
把localhost改成127.0.0.1成功

把localhost改成127.0.0.1后竟然连接成功了，开始陷入思考困局：localhost失败127.0.0.1却成功？

ping localhost 地址是127.0.0.1没错

打开hosts加入

复制代码代码如下:

127.0.0.1 qttc

使用qttc当主机连接也正常，唯独就不认localhost。
localhost连接方式不同导致

为了了解PHP连接数据库时，主机填写localhost与其它的区别阅读了大量资料，最后得知：

当主机填写为localhost时mysql会采用 unix domain socket连接
当主机填写为127.0.0.1时mysql会采用tcp方式连接
这是linux套接字网络的特性，win平台不会有这个问题

解决方法

在my.cnf的[mysql]区段里添加

复制代码代码如下:
protocol=tcp

保存重启MySQL，问题解决！
```

```
对接接口时  可以用这个去看参数
file_get_contents('php://input')
```

```
$res = app('db')->getQueryLog();
foreach ($res as $sql) {
    $tmp = str_replace("?", "'%s'", $sql['query']);
    array_unshift($sql['bindings'], $tmp);
    file_put_contents('../storage/logs/sql.log', call_user_func_array('sprintf', $sql['bindings']) . "\n\r", FILE_APPEND);
}
file_put_contents('../storage/logs/sql.log', "\n\r\n\r", FILE_APPEND);
```

```
// 打印表结构
select `TABLE_NAME`, `COLUMN_NAME`, `COLUMN_TYPE`, `IS_NULLABLE`, `COLUMN_COMMENT`, `COLUMN_KEY`, `EXTRA` from `information_schema`.`columns` where `table_schema` = ? group by `TABLE_NAME
```

```
MySQL开启日志

2、开启日志模式

-- 1、设置

-- SET GLOBAL log_output = 'TABLE';SET GLOBAL general_log = 'ON';  //日志开启

-- SET GLOBAL log_output = 'TABLE'; SET GLOBAL general_log = 'OFF';  //日志关闭

-- 2、查询

SELECT * from mysql.general_log ORDER BY event_time DESC;

-- 3、清空表（delete对于这个表，不允许使用，只能用truncate）

-- truncate table mysql.general_log;

```


```
http://phpstorm.tips/tips/5-jump-to-next-previous-method

关于快捷键， 请确认 没有其他软件占用快捷键

php strom快捷键

mac                                           win

将新光标添加到光标当前下一个词的出现处
ctrl + G                                      alt + j
删除最后添加的光标。
ctrl + shift + G                              shift + ctrl + j

alt + 拖动光标，选择多行光标

左侧导航的 锁定的按钮，快速定位文件

快速定位方法和属性
cmd + F12                                      ctrl + F12


```
