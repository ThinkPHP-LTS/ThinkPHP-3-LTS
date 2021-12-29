# ThinkPHP-3-LTS    （ThinkPHP 3.x 长期支持版）

持续维护ThinkPHP 3.x 版本的语法，使用现代的composer等类库，但保持对原有语法和用法的兼容，以便此前程序可以平滑迁移升级。

本项目采用与官方原始版本一致的 Apache 2 开源协议。

路线图TODO：
------------
1. 目前发现PHP 7上有不兼容，准备修复PHP 7的不兼容；
2. 发现一些TP5、TP6的比较好的特性，进行引入
3. 关注和验证可能的漏洞情况，尝试修复。 增加一些主动防御的插件机制。

社区QQ群：
---------
群号：619288321


项目使用说明：
------------

① Composer 包地址： https://packagist.org/packages/thinkphp-lts/thinkphp-3-lts

② 到项目文件夹下使用执行composer安装命令

> composer require thinkphp-lts/thinkphp-3-lts dev-main


建立index.php文件如下

```
<?php

// 应用入口文件

// 检测PHP环境
if (version_compare(PHP_VERSION, '5.6.0', '<')) {
    die('require PHP > 5.6.0 !');
}

// 开启调试模式 建议开发阶段开启 部署阶段注释或者设为false
define('APP_DEBUG', true);

// 定义应用目录
define('APP_PATH', './Application/');

// 定义模板主题
define("DEFAULT_THEME","default");

// 定义模板文件默认目录
define("TMPL_PATH","./Template/".DEFAULT_THEME."/");

// 定义静态文件路径-建议使用CDN地址
define("STATIC_PATH","http://cdn.com/");

// 引入ThinkPHP入口文件
require './vendor/thinkphp-lts/thinkphp-3-lts/src/ThinkPHP/ThinkPHP.php';

// 亲^_^ 后面不需要任何代码了 就是如此简单

```

然后使用 php -S localhost:80 启动开发服务器，之后访问 http://localhost

正确后会返回

```
欢迎使用 ThinkPHP！
版本 V3.2.5
```

返回目录，即看到框架自动生成了 Application文件夹（项目初始化目录）

后续注意在.gitignore里忽略掉 vendor 目录



官方版本介绍
------------

官方原始代码地址：  https://github.com/top-think/thinkphp 

官方已经不在维护3.x版本，参见官网关于支持周期的说明博客：https://blog.thinkphp.cn/810718

官方该版本原始文档：https://www.kancloud.cn/manual/thinkphp  | 官网： https://www.thinkphp.cn/ | 早期的下载页面：https://www.thinkphp.cn/down.html

代码起始点介绍
--------------

本项目的代码起始点为官方的  3.2.5版本 https://github.com/top-think/thinkphp/releases/tag/v3.2.5 

官方在 3.2.5版本后，在最新的master分支还有几次关于路由的修改，但是并未发布新版；为了保持跟此前程序的兼容性，本项目（ThinkPHP-3-LTS）没有引入官方未发版的关于路由的几次代码修改。

3.2.5版本对应的详细提交id为： https://github.com/top-think/thinkphp/commit/45489acfa131cf47efa61e85be05bedc8c3c94cf

长期支持组织
------------
类似的项目还有5.0.x支持计划：https://github.com/ThinkPHP-LTS/ThinkPHP-5.0.x-LTS

