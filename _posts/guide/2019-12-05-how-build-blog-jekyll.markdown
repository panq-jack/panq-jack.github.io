---
layout:     post
title:      "用githubpages+jekyll搭建个人博客"
subtitle:   "Build Your Blog"
author:     "Jack Pan"
header-img: "img/guide/bg-github-pages-jekyllrb.png"
header-mask:  0.8
tags:
    - Guide
    - Web
---



## 利用 Github Pages 搭建个人博客

> 感谢 [Hubpro](https://github.com/huxpro)提供的博客模板
>
> 以及[BYQiu](https://www.jianshu.com/p/e68fba58f75c)提供的教程

### 前言

本文利用Github Pages 提供的Jekyll 来搭建个人博客，操作简单快速，同时感谢 Hubpro 提供的模板。

下面开始基于模板的个人博客搭建。

### 预览   [Jack Pan Blog](https://panq-jack.github.io)



### 主题选择及配置

#### 注册或登录你的 Github 账号

#### 创建你的博客github仓库

- 寻找合适的模板主题，可以在[JekyllThemes](http://jekyllthemes.org/)上寻找
- 我这里是使用的[Huxpro](https://github.com/Huxpro/huxpro.github.io)的主题
  	- 打开主题repo，点击右上角的 `Fork`
  	- 等待一段时间，完成后点击`Setting` , 修改为你的repo，如：username.github.io
- clone到本地
  - 建议使用 Git 工具， 将repo clone到本地

#### repo结构

![blog-repo-structure](/img/guide/blog-repo-structure.png)

其中：

- `_config.yml` 全局配置文件
- `_posts` 放置博客文章的文件夹
- `img` 存放图片的文件夹

更多请查看官方文档   [Jekyll官方文档](https://www.jekyll.com.cn/docs/structure/)



### 安装开发工具:  ruby, jekyll, git 等

#### 安装ruby

- mac 系统已预安装，查看是否安装可在命令行输入 `ruby -v` 
- 若无安装，可在官网下载安装 [官网下载地址](https://www.ruby-lang.org/en/downloads/)， 并配置环境变量 .bash_profile

安装 RubyGems

- mac 系统已预安装，查看是否安装可在命令行输入 `gem -v` 
- 若无安装，可在官网下载安装 [官网下载地址](https://rubygems.org/pages/download)

#### 安装 Jekyll

- 执行  `gem install bundler jekyll`

若出现 `no permission` 相关的错误， 则使用 

> sudo gem install bundler jekyll

若出现报错：

```
ERROR:  Error installing jekyll:
ERROR: Failed to build gem native extension.
```

是因为缺少 ` Xcode-select `, 执行  (若安装过程中提示网络错误，可能是需要翻墙)

> ```csharp
> xcode-select --install
> ```



### 本地预览个人博客

- 到本地repo目录，执行

  > jekyll serve

  此时可能会报错如下：

  ```
   panq-jack.github.io git:(master) ✗ jekyll serve
  Configuration file: /Users/i520130/Documents/JavaProjects/githubpages/panq-jack.github.io/_config.yml
    Dependency Error: Yikes! It looks like you don't have jekyll-paginate or one of its dependencies installed. In order to use Jekyll as currently configured, you'll need to install this gem. If you've run Jekyll with `bundle exec`, ensure that you have included the jekyll-paginate gem in your Gemfile as well. The full error message from Ruby is: 'cannot load such file -- jekyll-paginate' If you run into trouble, you can find helpful resources at https://jekyllrb.com/help/!
                      ------------------------------------------------
        Jekyll 4.0.0   Please append `--trace` to the `serve` command
                       for any additional information or backtrace.
                      ------------------------------------------------
  ```

  是因为缺少依赖，那么执行

  > sudo gem install jekyll-paginate

​  若出现：
  >  Server address: http://127.0.0.1:4000/

​     则表示部署成功，在浏览器输入上述url即可查看

###  配置个人博客

#### 修改`_config_yml`

![blog-config](/img/guide/blog-config.png)


#### 留言系统

#### 网页统计

#### 自定义域名







### 参考文献

- [Jekyll](https://jekyllrb.com/)
- [Github Pages](https://pages.github.com/)
- [Liquid](https://help.shopify.com/en/themes/liquid/basics)
- [Clean-blog-jekyll-theme](https://github.com/BlackrockDigital/startbootstrap-clean-blog-jekyll)






