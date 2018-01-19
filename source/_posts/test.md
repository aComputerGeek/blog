---
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
批量入库时报错：prepared statement contains too many placeholders
原因：占位符的个数大于mysql对占位符的最高限制65535。
  条数 * 字段数
```

```
laravel  App\Exceptions\Handler::render  方法可以自定义错误返回信息 有时间仔细看下文档，读laravel
```

```
小程序框架
https://tencent.github.io/wepy/
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
代理网站
https://free-ss.site/
```
