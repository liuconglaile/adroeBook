---
layout: default
title: 按钮
parent: UI组件
nav_order: 2
---

# Buttons
{: .no_toc }

## 目录
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 基本按钮样式

### 看起来像按钮的链接

<div class="code-example" markdown="1">
[链接按钮](http://example.com/){: .btn }

[链接按钮](http://example.com/){: .btn .btn-purple }
[链接按钮](http://example.com/){: .btn .btn-blue }
[链接按钮](http://example.com/){: .btn .btn-green }

[Link button](http://example.com/){: .btn .btn-outline }
</div>
```markdown
[链接按钮](http://example.com/){: .btn }

[链接按钮](http://example.com/){: .btn .btn-purple }
[链接按钮](http://example.com/){: .btn .btn-blue }
[链接按钮](http://example.com/){: .btn .btn-green }

[链接按钮](http://example.com/){: .btn .btn-outline }
```

### 按钮元素

GitHub Flavored Markdown不支持该`button`元素, 因此您必须为此使用内联HTML:

<div class="code-example">
<button type="button" name="button" class="btn">按钮元素</button>
</div>
```html
<button type="button" name="button" class="btn">Button element</button>
```

---

## 通过按钮使用实用程序

### Button size

将按钮包装在使用 [font-size 实用程序类]({{ site.baseurl }}{% link docs/utilities/typography.md %}) 缩放按钮的容器中:

<div class="code-example" markdown="1">
<span class="fs-6">
[Big ass button](http://example.com/){: .btn }
</span>

<span class="fs-3">
[Tiny ass button](http://example.com/){: .btn }
</span>
</div>
```markdown
<span class="fs-8">
[Link button](http://example.com/){: .btn }
</span>

<span class="fs-3">
[Tiny ass button](http://example.com/){: .btn }
</span>
```

### 按钮之间的间距

使用 [margin utility classes]({{ site.baseurl }}{% link docs/utilities/layout.md %}#spacing) 在同一块中的两个按钮之间添加间距.

<div class="code-example" markdown="1">
[带空格的按钮](http://example.com/){: .btn .btn-purple .mr-2 }
[按钮 ](http://example.com/){: .btn .btn-blue .mr-2 }

[具有更大空间的按钮](http://example.com/){: .btn .btn-green .mr-4 }
[按钮 ](http://example.com/){: .btn .btn-blue }
</div>
```markdown
[带空格的按钮](http://example.com/){: .btn .btn-purple .mr-2 }
[按钮 ](http://example.com/){: .btn .btn-blue }

[具有更大空间的按钮](http://example.com/){: .btn .btn-green .mr-4 }
[按钮 ](http://example.com/){: .btn .btn-blue }
```
