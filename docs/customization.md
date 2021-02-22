---
layout: default
title: 定制
nav_order: 6
---

# 定制
{: .no_toc }

## 目录
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 配色方案
{: .d-inline-block }

新
{: .label .label-green }

Just the Docs 支持两种配色方案: light (default), 和 dark.

要启用配色方案, 请使用 `color_scheme` 在您的站点`_config.yml` 文件中设置参数:

#### 例
{: .no_toc }

```yaml
# Color scheme currently only supports "dark" or nil (default)
color_scheme: "dark"
```
<button class="btn js-toggle-dark-mode">查看深色方案</button>

<script type="text/javascript" src="{{ "/assets/js/dark-mode-preview.js" | absolute_url }}"></script>

## 特定的视觉定制

要自定义网站的外观，请`_sass/custom/custom.scss`在编辑器中打开以查看是否存在可以覆盖的变量. 大多数样式（如字体,颜色,间距等）均来自这些变量. 要覆盖特定变量,请取消注释其行并更改其值。

例如,要将链接颜色从紫色默认值更改为蓝色,请打开`_sass/custom/custom.css`并`$link-color`在line上找到变量`50`. 取消注释, 然后将其值更改为我们的`$blue-000`变量或您选择的其他阴影.

#### 例
{: .no_toc }

```scss
// ...
//
// $body-text-color: $grey-dk-100;
// $body-heading-color: $grey-dk-300;
$link-color: $blue-000;
//
// ...
```

_Note:_ `_sass/support/variables.scss` 建议不要直接在其中编辑变量, 否则可能导致其他依赖项失败.

## 替代样式

对于未定义为变量的样式, 您可能需要修改特定的CSS类. 要在级联末尾添加自己的CSS替代, 请编辑`_sass/overrides.scss`. 这将允许所有替代保存在单个文件中, 并且任何上游更改仍将应用。

例如, 如果您想添加自己的样式来打印页面, 则可以添加以下样式.

#### 例
{: .no_toc }

```scss
// Print-only styles.
@media print {
  .side-bar, .page-header { display: none; }
  .main-content { max-width: auto; margin: 1em;}
}
```
