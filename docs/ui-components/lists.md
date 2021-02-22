---
layout: default
title: 列表
parent: UI组件
nav_order: 5
---

# Lists
{: .no_toc }

## 目录
{: .no_toc .text-delta }

1. TOC
{:toc}

---

大多数列表可以使用纯Markdown呈现.

## 无序列表

<div class="code-example" markdown="1">
- Item 1
- Item 2
- Item 3

_or_

* Item 1
* Item 2
* Item 3
</div>
```markdown
- Item 1
- Item 2
- Item 3

_or_

* Item 1
* Item 2
* Item 3
```

## 清单列表

<div class="code-example" markdown="1">
1. Item 1
1. Item 2
1. Item 3
</div>
```markdown
1. Item 1
1. Item 2
1. Item 3
```

## 任务列表

<div class="code-example" markdown="1">
- [ ] 你好, 这是个待办事项
- [ ] 你好, 这是另一个待办事项
- [x] 再见, 这个项目完成了
</div>
```markdown
- [ ] 你好, 这是个待办事项
- [ ] 你好, 这是另一个待办事项
- [x] 再见, 这个项目完成了
```

## 自定义列表

定义列表需要HTML语法, 并且GitHub Flavored Markdown编译器不支持定义列表.

<div class="code-example" markdown="1">
<dl>
<dt>姓名</dt>
<dd>莫子铭</dd>
<dt>生日</dt>
<dd>1952</dd>
<dt>出生地</dt>
<dd>茂名</dd>
<dt>颜色</dt>
<dd>黄色</dd>
</dl>
</div>
```html
<dl>
  <dt>姓名</dt>
  <dd>莫子铭</dd>
  <dt>生日</dt>
  <dd>1952</dd>
  <dt>出生地</dt>
  <dd>茂名</dd>
  <dt>颜色</dt>
  <dd>黄色</dd>
</dl>
```
