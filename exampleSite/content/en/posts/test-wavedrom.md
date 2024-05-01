---
title: "Wavedrom support"
date: 2024-05-01T18:45:29+08:00
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
- wavedrom
---

## Introduction

WaveDrom is a Free and Open Source online digital timing diagram (waveform) rendering engine that uses javascript, HTML5 and SVG to convert a WaveJSON input text description into SVG vector graphics.

<br>

## Examples

````markdown
```wave
{
  "signal": [ {"name": "CLK", "wave": "p.....|..."},
            {"name":"DAT", "wave":"x.345x|=.x", "data":["A","B","C","D"]},
            {"name": "REQ", "wave": "0.1..0|1.0"},
            {},
            {"name": "ACK", "wave": "1.....|01."}
]}
```
````

```wave
{
  "signal": [ {"name": "CLK", "wave": "p.....|..."},
            {"name":"DAT", "wave":"x.345x|=.x", "data":["A","B","C","D"]},
            {"name": "REQ", "wave": "0.1..0|1.0"},
            {},
            {"name": "ACK", "wave": "1.....|01."}
]}
```
