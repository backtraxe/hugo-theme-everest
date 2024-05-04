---
title: "Hugo Archetypes"
date: 2024-05-04T02:50:31+08:00
lastmod: 2024-05-04T02:50:31+08:00
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

## What is an archetype

An archetype is a template for new content. This is an archetype example:

```markdown
---
title: '{{ replace .File.ContentBaseName `-` ` ` | title }}'
date: '{{ .Date }}'
draft: true
---
```

A markdown file consists of front matter. The front matter at the top of markdown file is metadata.

## Why use archetypes



## How does archetype work

When you create new content, Hugo evaluates the template actions within the archetype. For example:

```bash {linenos=false}
hugo new content posts/my-first-post.md
```

Hugo replaces the template config and creates this content file:

```markdown
---
title: My First Post
date: "2024-05-04T19:53:57+08:00"
draft: true
---
```

## How to configure archetypes

## References

1. [Archetypes | Hugo](https://gohugo.io/content-management/archetypes/)
2. [Front matter | Hugo](https://gohugo.io/content-management/front-matter/)
