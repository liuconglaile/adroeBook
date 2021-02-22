---
layout: default
title: 导航结构
nav_order: 5
---

# 导航结构
{: .no_toc }

## 目录
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 主导航

Just the Docs站点的主要导航在大屏幕页面的左侧, 在小屏幕顶部(点击后). 主导航的结构可以适应多级菜单系统(带有子页面的页面).

默认情况下，除非定义了父页面，否则所有页面将在主导航中显示为顶级页面(请参阅 [带子页面](#pages-with-children)).

---

## 订制页面

要指定页面顺序, 请`nav_order`在页面的YAML前题中使用参数.

#### 例
{: .no_toc }

```yaml
---
layout: default
title: Customization
nav_order: 4
---
```

---

## 排除页面

对于您不希望包含在主导航中的特定页面, 例如404页面或登录页面, 请`nav_exclude: true`在该页面的YAML前题中使用该参数。

#### 例
{: .no_toc }

```yaml
---
layout: default
title: 404
nav_exclude: true
---
```

---

## 子页面

有时您会想要创建一个包含许多子项的页面(一个部分). 首先,建议您将目录中相关的页面放在一起……例如, 在这些文档中, 我们将所有书面文档保留在`./docs`目录中, 并将每个部分保留在子目录, 如`./docs/ui-components` 和`./docs/utilities`. 这给了我们一个像这样的组织结构:

```
+-- ..
|-- (Jekyll files)
|
|-- docs
|   |-- ui-components
|   |   |-- index.md  (parent page)
|   |   |-- buttons.md
|   |   |-- code.md
|   |   |-- labels.md
|   |   |-- tables.md
|   |   +-- typography.md
|   |
|   |-- utilities
|   |   |-- index.md      (parent page)
|   |   |-- color.md
|   |   |-- layout.md
|   |   |-- responsive-modifiers.md
|   |   +-- typography.md
|   |
|   |-- (other md files, pages with no children)
|   +-- ..
|
|-- (Jekyll files)
+-- ..
```

在父页面上, 添加以下YAML前题参数:
-  `has_children: true` (告诉我们这是一个父页面)

#### 例
{: .no_toc }

```yaml
---
layout: default
title: UI Components
nav_order: 2
has_children: true
---
```

在这里, 我们设置了UI组件登录页面, 该页面可在处找到`/docs/ui-components`, 该页面具有子项, 在主导航中排名第二.

### 子页面
{: .text-gamma }

在子页面上, 只需将`parent:` YAML 前端问题设置为父页面的标题即可, 并​​设置导航顺序(此数字现在位于本节中).

#### 例
{: .no_toc }

```yaml
---
layout: default
title:
parent: UI Components
nav_order: 2
---
```

`"Buttons"`页面显示为`"UI Components"`的子级, 并在`"UI Components"`部分中排第二.

### 自动生成目录

默认情况下, 所有带有子页面的页面都会自动附加一个目录, 该目录在父页面内容之后列出子页面。要禁用此自动目录, 请`has_toc: false`在父页面的YAML前端设置.

#### 例
{: .no_toc }

```yaml
---
layout: default
title: UI Components
nav_order: 2
has_children: true
has_toc: false
---
```

### 子页面的子页面
{: .text-gamma }

子页面也可以有子页面(孙子). 这可以通过在子页面和孙子页面上使用类似的模式来实现.

1. 将`has_children`属性添加到子级.
2. 将`parent` 和 `grand_parent` 属性添加到孙子.

#### 例
{: .no_toc }

```yaml
---
layout: default
title: Buttons
parent: UI Components
nav_order: 2
has_children: true
---
```

```yaml
---
layout: default
title: Buttons Child Page
parent: Buttons
grand_parent: UI Components
nav_order: 1
---
```

这将创建以下导航结构:

```
+-- ..
|
|-- UI Components
|   |-- ..
|   |
|   |-- Buttons
|   |   |-- Button Child Page
|   |
|   |-- ..
|
+-- ..
```

---

## 辅助导航

要将辅助导航项添加到您的站点(在所有页面的右上角), 请将其添加到站点文件的`aux_nav` [配置选项]({{ site.baseurl }}{% link docs/configuration.md %}#aux-nav) `_config.yml`中.

#### 例
{: .no_toc }

```yaml
# Aux links for the upper right navigation
aux_links:
  "Just the Docs on GitHub":
    - "//github.com/pmarsceill/just-the-docs"
```

---

## 目录中的页内导航

要在文档页面上生成目录，您可以在Markdown中使用`{:toc}`Kramdown中的方法`<ol>`. 这将自动根据标题和标题级别生成指向页面各个部分的锚链接的有序列表. 在某些情况下, 您可能正在使用标题而又不想将其显示在目录中, 因此可以使用`{: .no_toc }`CSS类跳到特定的标题.


#### 例
{: .no_toc }

```markdown
# Navigation Structure
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}
```

此示例跳过目录中的页面名称标题(`#`), 以及内容列表本身(`##`)的标题, 因为它是多余的, 后面是目录本身.
