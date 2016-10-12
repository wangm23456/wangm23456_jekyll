---
layout: post
title: kramdown语法
---

<p class="message">
Github 更新 jekyll 3 后推荐使用 kramdown 和 Rouge 作为解析器和语法高亮器。
kramdown 是 markdown 的扩充版，语法上与markdown有所不同。
</p>

# 代码围栏

kramdown 使用前后三个 ~作为围栏而不是三个`，
通过在_config.yml 中设置：

```yaml
kramdown:
        input: GFM
```

就可以支持 github 句法，用`作为代码围栏.

在行内用单个`包含的内容也作为行内代码被解析。
另外也可以使用 highlight 标签。

如果出现代码被 Liquid 模板引擎过度解析，
则需要在围栏外加: `raw`  标记。

    import numpy

 Tab 或四个空格也可以使内容以块显示，但不能自动检测语言，所以不会高亮。

```html
<div class="highlighter-rouge"><pre class="highlight"><code>import numpy
</code></pre>
</div>
```

# 换行

一行空行被作为换行标志。另外，EOB标记也可以用来换行，
即：^单独一行，作为块元素结束标志。

# 链接

链接的url括号内用双引号可以添加鼠标悬停内容。

`[W-o-M](http://www.wangm23456.cc/ "wangm23456 blog")`

[W-o-M](http://www.wangm23456.cc/ "wangm23456 blog")

要链接到其他文章可以使用：

`[第一篇文章](% post_url 2016-10-11-linux_softguide  %)`

[第一篇文章](% post_url 2016-10-11-linux_softguide  %)

# 缩略语

即 Abbreviations (abbr) ，在文档中写：`*[abbr]: Abbreviations `。默认是大写。

*[abbr]: Abbreviations

# 表格

可以使用html的table元素，或用markdown句法：

```
|name|year|job
:-:|:-|-:
|year| 2016 |std
```

|name|year|job
:-:|:-|-:
|year| 2016 |std

其中的冒号用于控制左右居中对齐。

# 文本

`**加粗**`  `*斜体*`  `_斜体_`  `~~删除线~~`

**加粗**  ，*斜体*，_斜体_，~~删除线~~`。