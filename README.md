# JSimple

[![Build Status](https://travis-ci.org/tangkunyin/hexo-theme-jsimple.svg?branch=master)](https://travis-ci.org/tangkunyin/hexo-theme-jsimple)


**适用于Hexo的三栏简书式主题。支持响应式、站内搜索、多说评论、文章浏览统计以及白天和夜间模式**.

[**☞ 一睹为快**](https://blog.wfyvv.com)



<!--more-->

## 安装步骤

1. 从 GitHub 下载代码

```shell
 $ git clone https://github.com/wilcool/hexo-theme-jsimple.git themes/jsimple
```
2. 去主题中开启

在`_config.yml`中更改 `theme` 字段为 `jsimple`.

请在站点配置文件中，手动添加依赖： `"hexo-generator-json-content": "^2.2.0"` ，搜索会用到此依赖。

3. 更新主题

```shell
$ cd themes/jsimple
$ git pull
```


## 配置

便于快速上手, 直接看我的 [网站备份](https://github.com/shuoit/blog) 可能更方便。好多朋友下载主题使用报错，戳那里最直接。

### 重要的配置说明

#### 1. fullHttps: 一个布尔值( `true` or `false`)

全站强制性`https`访问，意味着网页中**Content-Security-Policy为upgrade-insecure-requests**。好处是当你忘记引用正确的https资源时它会帮你自动转成https。

但是如果你在本地调试，或者你的线上服务器不支持`https`，请把该项设置成`false`，否则主题中的css和js等资源将无法被正确引用。你打开的首页将因为加载不到css变得异常难看。

#### 2. 文章模板

站点的对应的`scaffolds`文件夹下的`post.md`模板，需要手动加入`categories`和`tags`，并设置值。这样能确保你某篇文章属于哪个分类。
我的`post.md`文件如下
```
title: {{ title }}
date: {{ date }}
tags: [] 
categories: []
photos: 
  - /images/blog/logo.png #首页显示图片
originAuthor: XX #原谅作者 可以空
originLink: http://www.wfyvv.com #原谅出处 可以空
```
'page.md'文件如下：
```
title: {{ title }}
date: {{ date }}
comments: false #是否开启评论
```

#### 3. menu: Map值
菜单分为左侧菜单和顶部菜单。主题中的配置顺序决定网站导航菜单顺序。
左侧菜单如下：
```
leftPagesMenu:
- uri: archives
  title: 归档
  faName: fa-archives
- uri: categories
  title: 分类
  faName: fa-book
- uri: tags
  title: 标签
  faName: fa-tags
- uri: about
  title: 关于
  faName: fa-question-circle
```
顶部菜单如下：
```
topMenu:
   图册: pictures
   简历: resume
```
顶部菜单若不配置，默认显示一个首页菜单。无论左侧菜单或顶部菜单，均需要在`public`文件夹下新建对应文件夹，并添加`index.md`。
若要关闭评论，需在`index.md`头部添加comments: false


## 浏览器支持

![](https://raw.githubusercontent.com/iTimeTraveler/hexo-theme-hipaper/master/source/preview/browser-support.png?raw=true)



## 鸣谢

[hexo-theme-jsimple](https://github.com/tangkunyin/hexo-theme-jsimple)




