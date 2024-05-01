---
title: "Graphviz support"
date: 2024-05-01T18:30:15+08:00
description: " "
draft: false
hideToc: false
enableToc: true
enableTocContent: false
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
libraries:
- viz
---

## Enable Graphviz

```yaml
libraries:
- viz
```

<br>

## Examples

````markdown
```viz-dot
digraph G {
    subgraph cluster_0 {
        style = filled;
        color = lightgrey;
        node [style=filled, color=white];
        a0 -> a1 -> a2 -> a3;
        label = "process #1";
    }

    subgraph cluster_1 {
        node [style=filled];
        b0 -> b1 -> b2 -> b3;
        label = "process #2";
        color = blue
    }

    start -> a0;
    start -> b0;
    a1 -> b3;
    b2 -> a3;
    a3 -> a0;
    a3 -> end;
    b3 -> end;

    start [shape=square];
    end [shape=square];
}
```
````

```viz-dot
digraph G {
    subgraph cluster_0 {
        style = filled;
        color = lightgrey;
        node [style=filled, color=white];
        a0 -> a1 -> a2 -> a3;
        label = "process #1";
    }

    subgraph cluster_1 {
        node [style=filled];
        b0 -> b1 -> b2 -> b3;
        label = "process #2";
        color = blue
    }

    start -> a0;
    start -> b0;
    a1 -> b3;
    b2 -> a3;
    a3 -> a0;
    a3 -> end;
    b3 -> end;

    start [shape=square];
    end [shape=square];
}
```
