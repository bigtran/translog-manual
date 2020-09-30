# 站点配置信息

site.yml 文件，主要用来配置站点的基本信息。

## 示例site.yml文件

```
---
title: Another translog site.
description:
# 基础路径，必须以“/”结尾
baseURL: http://bigtran.opmonitor.com/
# &copy; 后面的信息
copyright: bigtran 2020-
# 配置首页页面路径，是index，还是achieves，还是某一篇文章？默认是index
home:index
# 模板文件
theme: default
---
```

## site.yml 的扩充

site.yml 可以按需扩充，和站点有关的信息都可以在 site.yml中进行配置。
这是后面计划支持的一些扩充：
- language: 语言配置
- plugin: 要加载的插件
- menu: 预定义的导航
- taxonomies: 分类目录，标签（好像也没有必要提前定义）
- atom_url
- rss2_url
- pingback_url
- charset

## 获取 site.yml中间的参数

```
<?php _siteinfo('title'); ?> : 获取站点名称(Title)
<?php _siteinfo('baseURL'); ?> : 获取站点基础url(baseURL)
<?php _siteinfo('theme'); ?> : 获取站点模板地址(theme)
```
