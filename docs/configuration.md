---
layout: default
title: 组态
nav_order: 2
---

# 组态
{: .no_toc }


Just the Docs 具有一些特定的配置参数，可以在您的Jekyll网站的`_config.yml`文件中定义这些参数.
{: .fs-6 .fw-300 }

## 目录
{: .no_toc .text-delta }

1. TOC
{:toc}

---


以该站点的 [_config.yml](https://github.com/pmarsceill/just-the-docs/tree/master/_config.yml) 文件为例.

## 网站徽标

```yaml
# 将路径/ URL设置为将显示的logo而不是标题
logo: "/assets/images/just-the-docs.png"
```

## 搜索

```yaml
# 启用或禁用站点搜索
# 支持true（默认）或false
search_enabled: true

# 启用对带连字符的搜索词的支持:
search_tokenizer_separator: /[\s/]+/

```

## 辅助链接

```yaml
# 右上方导航的辅助链接
aux_links:
  "Just the Docs on GitHub":
    - "//github.com/pmarsceill/just-the-docs"
```

## 标题锚链接

```yaml
# 标题锚点链接显示在页面内容中的h1-h6标签上
# 允许用户深入链接到页面上的特定标题.
#
# 支持true（默认）或false/nil
heading_anchors: true
```

## 页脚内容

```yaml
# Footer content appears at the bottom of every page's main content
footer_content: "Copyright &copy; 2017-2019 Patrick Marsceill. Distributed by an <a href=\"https://github.com/pmarsceill/just-the-docs/tree/master/LICENSE.txt\">MIT license.</a>"
```

## 配色方案

```yaml
# Color scheme currently only supports "dark" or nil (default)
color_scheme: "dark"
```
<button class="btn js-toggle-dark-mode">预览深色方案</button>

<script type="text/javascript" src="{{ "/assets/js/dark-mode-preview.js" | absolute_url }}"></script>

有关更多信息, 请参见 [自定义]({{ site.baseurl }}{% link docs/customization.md %}).

## 谷歌分析

```yaml
# Google Analytics Tracking (optional)
# e.g, UA-1234567-89
ga_tracking: UA-5555555-55
```
