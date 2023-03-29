---
date: 2018-02-07T18:30:00+06:00
lastmod: 2022-09-22T18:00:00+06:00
title: 挂件功能
authors: ["muniftanjim"]
categories:
  - 特征
tags:
  - config
  - 挂件
toc: true

---
Minimo supports _**Widgets**_ that you can place on specific _**Widget Areas**_.

## Available Widgets

Minimo has the following built-in Widgets:

  Name             |  Slug
 ----------------- | -----------------
 1. About          | `about`
 2. Breadcrumbs    | `breadcrumbs`
 3. Recent Posts   | `recent_posts`
 4. Search         | `search`
 5. Sidebar Menu   | `sidebar_menu`
 6. Social Menu    | `social_menu`
 7. Taxonomy Cloud | `taxonomy_cloud`

### Widget 配置 Options

Here are the 配置 options available for the Widgets:

#### Widget: About

- `about` [`Map`]:
  - `title` [`String`]: Title  
     _default: `.Site.Title`_
  - `description` [`String`]: Description  
    _default: `.Site.Params.info.description`_
  - `logo` [`String`]: path/url of Logo  
    _default: `"images/logo.png"`_

#### Widget: Breadcrumbs

- `breadcrumbs` [`Map`]:
  - `separator` [`String`]: Breadcrumb separator  
     _default: `"/"`_
  - `excludeParents` [`Array` of `String`s]:  Types of parents to exclude  
    _default: `["page"]`_

#### Widget: Recent Posts

- `recent_posts` [`Map`]:
  - `title` [`String`]: Title  
    _default: `"Recent Posts"`_
  - `length` [`Integer`]: Number of posts to show  
    _default: `5`_
  - `excludeTypes` [`Array` of `String`s]:  Types of posts to exclude  
    _default: `["page"]`_

#### Widget: 搜索

- `search` [`Map`]:
  - `title` [`String`]: Title  
    _default: `"Search"`_

#### Widget: Sidebar Menu

- `sidebar_menu` [`Map`]:
  - `title` [`String`]: Title  
    _default: `""`_
  - `mirror` [`String`]: Name of menu to mirror (e.g. `"main"`)  
    _default: `""`_

#### Widget: Social Menu

- `social_menu` [`Map`]:
  - `title` [`String`]: Title  
    _default: `""`_
  - `platforms` [`Array` of `String`s]: Social platform to show

#### Widget: Taxonomy Cloud

- `taxonomy_cloud` [`Map`]:
  - `title` [`String`]: Title  
    _default: Plural Name for `taxonomyCloud.taxonomy`_
  - `taxonomy` [`String`]: Taxonomy to show  
    _default: `.Site.Params.info.description`_
  - `shuffle` [`Boolean`]: Shuffle Taxonomy Terms  
    _default: `true`_

## Available Widget Areas

  Name    |  Slug
 -------- | ----------
 Header   | `header`
 Homepage | `homepage`
 Sidebar  | `sidebar`
 Footer   | `footer`

You can add Widgets to Widget Areas from your **`config.toml`** file:

```toml
[params.widgets]
header = ["breadcrumbs"]
homepage = ["recent_posts"]
sidebar = ["about","taxonomy_cloud"]
footer = ["social_menu"]
```

The syntax for adding Widgets to Widget Areas is:

```toml
widget_area_slug = [ widget_slug_1, widget_slug_2, ...]
```

## Widgets 配置 File

Minimo picks up Widgets' 配置 from the **`/data/config/widgets.toml`** file.

Here's the _Widgets Config file_ for this site:

**`/data/config/widgets.toml`**

{{< file "data/config/widgets.toml" >}}

If 配置 for any Widgets are missing in this file, Minimo will fallback to the default 配置 for those Widgets.

Go wild!
