---
title: "Hugo shortcodes"
date: 2024-05-01T02:11:20+08:00
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
- hugo
tags:
- hugo
series:
- hugo
image:
---

## Introduction

Shortcodes are simple snippets inside your content files calling built-in or custom templates.

## Usage

<!-- {{< highlight html >}}
```html
<p>Hello <strong>World!</strong></p>
```
{{< /highlight  >}}

{{% highlight html %}}
```html
<p>Hello <strong>World!</strong></p>
```
{{% /highlight  %}} -->

- `<>`: Content keep the raw markdown and HTML.

```markdown
{{</* shortcode params */>}}
<!-- content -->
{{</* /shortcode */>}}
```

- `%%`: Content render markdown and HTML, not raw content.

```markdown
{{%/* shortcode params */%}}
<!-- content -->
{{%/* /shortcode */%}}
```

## Hugo embedded shortcodes

### figure

Embed an image.

```markdown
{{</* figure src="elephant.jpg"
           title="An elephant at sunset"
           caption=""
           link=""
           target="_blank"
           rel=""
           alt=""
           height=100%
           width=100% */>}}
```

### gist

Embed a [Github Gist](https://gist.github.com/discover), namely a code snippet.

```markdown
<!-- https://gist.github.com/backtraxe/5cd0b62d3a5d31b02971b991e658517a -->
{{</* gist backtraxe 5cd0b62d3a5d31b02971b991e658517a reverse_linked_list.cpp */>}}
```

{{< gist backtraxe 5cd0b62d3a5d31b02971b991e658517a reverse_linked_list.cpp >}}

### highlight

Refer to [Hugo syntax highlighting](./hugo-syntax-highlight.md).

### instagram

Embed an [Instagram](https://www.instagram.com/) post.

```markdown
<!-- https://www.instagram.com/p/C2ESOA-Lgyi -->
{{</* instagram C2ESOA-Lgyi */>}}
```

{{< instagram C2ESOA-Lgyi >}}

### twitter

Embed a [Twitter](https://twitter.com/) tweet.

```markdown
<!-- https://twitter.com/realmadrid/status/1785262829760885226 -->
{{</* twitter user="realmadrid" id="1785262829760885226" */>}}
```

{{< twitter user="realmadrid" id="1785262829760885226" >}}

### vimeo

Embed a [Vimeo](https://vimeo.com/) video.

```markdown
<!-- https://vimeo.com/261660348 -->
{{</* vimeo 261660348 */>}}
```

{{< vimeo 261660348 >}}

### youtube

Embed a [YouTube](https://www.youtube.com/) video.

```markdown
<!-- https://www.youtube.com/watch?v=SX_ViT4Ra7k -->
{{</* youtube id=SX_ViT4Ra7k
            start=60
            end=90
            loading=lazy
            allowFullScreen=true
            autoplay=false
            mute=true
            controls=true
            loop=false */>}}
```

{{< youtube id=SX_ViT4Ra7k
            start=60
            end=90
            loading=lazy
            allowFullScreen=true
            autoplay=false
            mute=true
            controls=true
            loop=false >}}

<br>

## Everest custom shortcodes

### alert

Colored box.

```markdown
{{</* alert theme="danger" */>}}danger alert{{</* /alert */>}}

{{</* alert theme="warning" */>}}warning alert{{</* /alert */>}}

{{</* alert theme="info" */>}}info alert{{</* /alert */>}}

{{</* alert theme="success" */>}}success alert{{</* /alert */>}}
```

{{< alert theme="danger" >}}danger alert{{< /alert >}}

{{< alert theme="warning" >}}warning alert{{< /alert >}}

{{< alert theme="info" >}}info alert{{< /alert >}}

{{< alert theme="success" >}}success alert{{< /alert >}}

### box

Don't render markdown and HTML, keep the raw content.

```markdown
{{</* box */>}}
This is **box** shortcode.
{{</* /box */>}}
```

{{< box >}}
This is **box** shortcode.
{{< /box >}}

### boxmd

Render markdown and HTML, not keep the raw content.

```markdown
{{</* boxmd */>}}
This is **boxmd** shortcode.
{{</* /boxmd */>}}
```

{{< boxmd >}}
This is **boxmd** shortcode.
{{< /boxmd >}}

### button

<!-- todo -->
{{< button >}}
submit
{{< /button >}}

### codes & code

Make it easy to switch between different code.

````markdown
{{</* codes java javascript */>}}
{{</* code */>}}

```java
System.out.println('Hello World!');
```

{{</* /code */>}}

{{</* code */>}}

```javascript
console.log('Hello World!');
```

{{</* /code */>}}
{{</* /codes */>}}
````

{{< codes java javascript >}}
{{< code >}}

```java
System.out.println('Hello World!');
```

{{< /code >}}

{{< code >}}

```javascript
console.log('Hello World!');
```

{{< /code >}}
{{< /codes >}}

### color

<!-- todo -->
{{< color >}}
This is a colored sentence.
{{< /color >}}

### expand

Click to expand.

```markdown
{{</* expand "Click to expand" */>}}
inner content
{{</* /expand */>}}
```

{{< expand "Click to expand" >}}
inner content
{{< /expand >}}

### notice

Colored banner.

```markdown
{{</* notice error */>}}error notice{{</* /notice */>}}

{{</* notice warning */>}}warning notice{{</* /notice */>}}

{{</* notice info */>}}info notice{{</* /notice */>}}

{{</* notice success */>}}success notice{{</* /notice */>}}
```

{{< notice error >}}error notice{{< /notice >}}

{{< notice warning >}}warning notice{{< /notice >}}

{{< notice info >}}info notice{{< /notice >}}

{{< notice success >}}success notice{{< /notice >}}

### tabs & tab

Make it easy to switch between different tab.

````markdown
{{</* tabs Windows MacOS Linux */>}}
{{</* tab */>}}

#### Windows

- Developer: Microsoft
- Open-source: false

{{</* /tab */>}}

{{</* tab */>}}

#### MacOS

- Developer: Apple
- Open-source: false

{{</* /tab */>}}

{{</* tab */>}}

#### Linux

- Developer: Global Community
- Open-source: true

{{</* /tab */>}}
{{</* /tabs */>}}
````

{{< tabs Windows MacOS Linux >}}
{{< tab >}}

#### Windows

- Developer: Microsoft
- Open-source: false

{{< /tab >}}

{{< tab >}}

#### MacOS

- Developer: Apple
- Open-source: false

{{< /tab >}}

{{< tab >}}

#### Linux

- Developer: Global Community
- Open-source: true

{{< /tab >}}
{{< /tabs >}}
