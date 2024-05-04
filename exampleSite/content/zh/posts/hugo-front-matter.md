---
title: "Hugo Front Matter"
date: 2024-05-04T20:03:38+08:00
lastmod: 2024-05-04T20:03:38+08:00
description:
draft: false
hideToc: false
enableToc: true
enableTocContent: false
tocFolding: false
tocPosition: inner
tocLevels: ["h2", "h3", "h4"]
author: Backtraxe
authorEmoji:
image:
pinned: false
weight:
categories:
-
tags:
- hugo
series:
-
libraries:
-
---

## 什么是 front matter ？

Front matter 是以 Hugo 可以理解的格式在每个博客文件顶部的元数据。它通常包括标题、日期、作者和其他与文件内容相关的元数据信息。Hugo 使用 front matter 来确定如何处理和显示文件中的内容。

示例:

```markdown
---
title: "My First Post"
date: "2024-05-04T19:53:57+08:00"
draft: true
---
```

## 为什么使用 front matter ？

- 描述内容
- 丰富内容
- 与其他内容建立关系
- 控制网站的已发布结构
- 确定模板选择

## Front matter 类型

在 archetype 文件（`/archetypes/*`）中的 front matter 是 go 模板。

```markdown
---
title: '{{ replace .File.ContentBaseName `-` ` ` | title }}'
date: '{{ .Date }}'
draft: true
---
```

在普通博客文件（`/content/*`）中的 front matter 则是具体配置内容。

```markdown
---
title: "My First Post"
date: "2024-05-04T19:53:57+08:00"
draft: true
---
```

## 如何配置 front matter ？

### 模板

更多 archetypes 内容参考 [Hugo Archetypes](hugo-archetypes.md).

```markdown
---
title: '{{ replace .File.ContentBaseName `-` ` ` | title }}'
description:
date: '{{ .Date }}'
draft: true
params:
  author:
tags:
-
lastmod: '{{ .Date }}'
publishDate: '{{ .Date }}'
expiryDate:
type:
weight:
---
```

### 具体内容

```markdown
---
title: "My First Post"
description: "This is my first post."
date: "2024-05-04T19:53:57+08:00"
draft: true
params:
  author: Backtraxe
tags:
- hugo
lastmod: "2024-05-04T19:53:57+08:00"
publishDate: "2024-05-04T19:53:57+08:00"
expiryDate: "2099-05-04T19:53:57+08:00"
type: posts
weight: 1
---
```

### Everest 主题模板配置

```markdown
---
title: '{{ replace .File.ContentBaseName `-` ` ` | title }}'
date: '{{ .Date }}'
lastmod: '{{ .Date }}'
description:
draft: true
hideToc: false
enableToc: true
enableTocContent: false
tocFolding: false
tocPosition: inner
tocLevels: ["h2", "h3", "h4"]
author: Backtraxe
authorEmoji:
image:
pinned: false
weight:
categories:
-
tags:
-
series:
-
libraries:
-
---
```

## References

1. [Front matter | Hugo](https://gohugo.io/content-management/front-matter/)
