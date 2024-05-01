---
title: Markdown syntax guide
date: 2024-05-01T17:26:10+08:00
description: " "
draft: false
hideToc: false
enableToc: true
enableTocContent: false
tocPosition: inner
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
---

## Headings

```markdown
# H1

## H2

### H3

#### H4

##### H5

###### H6
```

<br>

## Blockquotes

### Blockquote without attribution

```markdown
> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Note** that you can use *Markdown syntax* within a blockquote.
```

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Note** that you can use *Markdown syntax* within a blockquote.

### Blockquote with attribution

```markdown
> Don't communicate by sharing memory, share memory by communicating.</p>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.
```

> Don't communicate by sharing memory, share memory by communicating.</p>
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

<br>

## Tables

```markdown
Name  | Age
------|------
Bob   | 27
Alice | 23
```

Name  | Age
------|------
Bob   | 27
Alice | 23

<br>

## Code Blocks

````markdown
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
```
````

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
```

<br>

## List Types

### Ordered List

```markdown
1. First item
2. Second item
3. Third item
```

1. First item
2. Second item
3. Third item

### Unordered List

```markdown
- List item
- Another item
- And another item
```

- List item
- Another item
- And another item

### Nested list

```markdown
- Item
  1. First Sub-item
  2. Second Sub-item
```

- Item
  1. First Sub-item
  2. Second Sub-item

<br>
