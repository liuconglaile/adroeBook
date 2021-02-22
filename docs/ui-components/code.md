---
layout: default
title: 代码块
parent: UI组件
nav_order: 6
---

# Code
{: .no_toc }

## 目录
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 内联代码

可以通过将代码包装在单个反勾中来内嵌呈现代码.

<div class="code-example" markdown="1">
Lorem ipsum dolor sit amet, `<inline code snippet>` adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
</div>
```markdown
Lorem ipsum dolor sit amet, `<inline code snippet>` adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
```

---

## 语法突出显示的代码块

使用Roky将Jekyll的内置语法高亮显示在色块中,方法是使用三个反引号,可注明语言名称:

<div class="code-example" markdown="1">
```js
// 带有语法突出显示的Java代码.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```
</div>
{% highlight markdown %}
```js
// 带有语法突出显示的Java代码.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```
{% endhighlight %}

---

## 带有渲染示例的代码块

为了演示前端代码, 有时显示该代码的渲染示例很有用.
在包含了需要显示渲染的项目样式之后，可以将`<div>`与`code-example`类一起使用, 后跟代码块语法.
如果要使用Markdown而不是HTML呈现输出, 请使用`markdown="1"`属性告诉Jekyll您正在呈现的代码将采用Markdown格式…这将获取元数据…


<div class="code-example" markdown="1">

<div class="code-example" markdown="1">

[Link button](http://example.com/){: .btn }

</div>
```markdown
[Link button](http://example.com/){: .btn }
```

</div>
{% highlight markdown %}
<div class="code-example" markdown="1">

[Link button](http://example.com/){: .btn }

</div>
```markdown
[Link button](http://example.com/){: .btn }
```
{% endhighlight %}
