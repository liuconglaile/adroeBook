---
# 随时向该文件添加内容和自定义前项.
# 要修改布局，请参见 https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: 简介
nav_order: 1
description: "Just Docs是具有内置搜索功能的自适应Jekyll主题，可轻松自定义并托管在GitHub Pages."
permalink: /
---

# 专注于编写好的文档
{: .fs-9 }

只是文档为您的文档提供了一个快速响应的Jekyll主题的入门指南，该主题易于自定义并托管在GitHub Pages.
{: .fs-6 .fw-300 }

[现在开始](#getting-started){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [在GitHub上查看](https://github.com/pmarsceill/just-the-docs){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## 入门

### 依赖关系

只是Docs是为静态站点生成器[Jekyll](https://jekyllrb.com)构建的. 查看 [快速入门指南](https://jekyllrb.com/docs/) 以获取更多信息. 只是Docs不需要特殊的插件,并且可以在GitHub Pages的标准Jekyll编译器上运行. 该[Jekyll SEO Tag plugin](https://github.com/jekyll/jekyll-seo-tag)默认情况下（无需运行任何特殊安装）注入SEO和开放图元数据的文档页面包括在内. 有关如何配置SEO和打开图元数据的信息, 请访问[Jekyll SEO标签使用指南](https://jekyll.github.io/jekyll-seo-tag/usage/).

### 快速入门: 用作GitHub Pages远程主题

1. 在 `_config.yml`设置[远程主题](https://blog.github.com/2017-11-29-use-any-theme-with-github-pages/)到您的Jekyll网站. 
```yaml
remote_theme: pmarsceill/just-the-docs
```
<small>您必须在仓库中启用GitHub Pages, 一个或多个Markdown文件以及一个 `_config.yml` 文件. [查看示例存储库](https://github.com/pmarsceill/jtd-remote)</small>

### 本地安装: 使用基于gem的主题

1. 安装Ruby Gem
```bash
$ gem install just-the-docs
```
```yaml
# .. or add it to your your Jekyll site’s Gemfile
gem "just-the-docs"
```
2. 仅将文档添加到您的Jekyll网站的 `_config.yml`
```yaml
theme: "just-the-docs"
```
3. _可选:_ 初始化搜索数据 (创建 `search-data.json`)
```bash
$ bundle exec just-the-docs rake search:init
```
3. 运行本地Jekyll服务器
```bash
$ jekyll serve
```
```bash
# .. 或者如果您使用的是Gemfile (bundler)
$ bundle exec jekyll serve
```
4. 在浏览器打开 [http://localhost:4000](http://localhost:4000)

如果您将站点托管在GitHub Pages上, [请在本地设置GitHub Pages和Jekyll](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll), 以便您可以更轻松地在开发环境中工作.

### 仅配置文档

- [查看配置选项]

---

## 关于该项目

Just the Docs 是 &copy; 2017-2019 by [Patrick Marsceill](http://patrickmarsceill.com).

### License执照

Just the Docs 是由 [MIT license](https://github.com/pmarsceill/just-the-docs/tree/master/LICENSE.txt)分发的.

