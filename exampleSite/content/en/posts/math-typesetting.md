---
title: Math typesetting
date: 2024-05-01T17:42:57+08:00
description: " "
draft: false
hideToc: false
enableToc: true
enableTocContent: false
author: Backtraxe
authorEmoji:
pinned: false
categories:
- cheatsheet
tags:
- cheatsheet
series:
- cheatsheet
image:
libraries:
- katex
math: true
---

## Enable KaTex

```yaml
libraries:
- katex
math: true
```

<br>

## Examples

### Inline

```markdown
$\varphi=\dfrac{1+\sqrt{5}}{2}=1.6180339887\dots$
```

$\varphi=\dfrac{1+\sqrt{5}}{2}=1.6180339887\dots$

### Block

```markdown
$$\varphi=1+\frac{1}{1+\frac{1}{1+\frac{1}{1+\cdots}}}$$
```

$$\varphi=1+\frac{1}{1+\frac{1}{1+\frac{1}{1+\cdots}}}$$

<br>

## References

1. [Supported TeX Functions](https://katex.org/docs/supported.html)
