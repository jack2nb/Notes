---
date: 2020-09-25T06:00:00+06:00
title: "hugo配置"
authors: ["jack"]
toc: true

categories:
  - hugo
  - 博客使用
tags:
  - hugo
   
 
 
---


## 配置博客
配置文件是`./config.toml`但是光修改配置文件是不能拥有漂亮的博客，
先需要选择一个主题,我选择了`minimo`作为主题并把文件放入
./themes/minimo文件夹内

### 使用主题
修改config.toml文件
```toml
theme = "minimo"
```

最好先试一下主题中提供的例子 ./themes/minimo/exampleSite
将例子文件复制博客所在目录即可
```toml
[languages]
[languages.zh]
lang = "zh"
languageName = "Chinese"
```
同时修改一下配置文件中的语言
 
### 启动组件
```toml
[params.widgets]
header = ["breadcrumbs"]
homepage = ["recent_posts"]
sidebar = ["about","search","sidebar_menu","taxonomy_cloud"]
footer = ["social_menu"]
[params.search]
client = "fuse" # algolia / fuse / lunr 开启查找功能

```
 