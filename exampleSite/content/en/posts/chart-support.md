---
title: "Chart support"
date: 2024-05-01T19:26:18+08:00
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
- chart
---

Simple yet flexible JavaScript charting for designers & developers

```chart
{
    "type": "bar",
    "data":
       {
        "labels": ["One", "Two", "Three", "Four", "Five", "Six"],
        "datasets": [{
            "label": "# of Votes",
            "data": [12, 19, 3, 5, 3, 8]
        }]
    }
}
```

```chart
    {
    "type": "line",
        "data": {
            "labels": ["One", "Two", "Three", "Four", "Five", "Six"],
            "datasets": [
            {
                "label": "# of Votes",
                "data": [12, 19, 3, 5, 2, 3],
                "backgroundColor":"transparent",
                "borderColor":"orange"
            },
            {
                "label": "Some other set",
                "data": [15, 8, 13, 5, 5, 9],
                "backgroundColor":"transparent",
                "borderColor":"#44ccff"
            }
            ]
        }
    }
```
