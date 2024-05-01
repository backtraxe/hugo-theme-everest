---
title: "Hugo syntax highlighting"
date: 2024-05-01T00:51:05+08:00
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

## Highlight shortcode

### Usage

- hugo shortcode

```markdown
{{</* highlight cpp "linenos=table, linenostart=199, hl_lines=8 15-17" */>}}
<!-- code -->
{{</* /highlight */>}}
```

- markdown highlight block

````markdown
```cpp {linenos=table, linenostart=199, hl_lines=[8, "15-17"]}
// code
```
````

### Attributes

- `linenos`: Line numbers. [`true`, `false`, `table`, `inline`]
- `hl_lines`: Highlighted line numbers.
- `linenostart`: Line number start, default 1.
- `anchorlinenos`: Set the line number clickable.
- `lineanchors`: Set the prefix string of the line number in anchor url.

<br>

## Examples

### Example 1

- code

````markdown
```cpp {linenos=table, linenostart=25, hl_lines=[4,"6-10"]}
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> hashtable;
        for (int i = 0; i < nums.size(); ++i) {
            auto it = hashtable.find(target - nums[i]);
            if (it != hashtable.end()) {
                return {it->second, i};
            }
            hashtable[nums[i]] = i;
        }
        return {};
    }
};
```
````

- result

```cpp {linenos=table, linenostart=25, hl_lines=[4,"6-10"]}
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> hashtable;
        for (int i = 0; i < nums.size(); ++i) {
            auto it = hashtable.find(target - nums[i]);
            if (it != hashtable.end()) {
                return {it->second, i};
            }
            hashtable[nums[i]] = i;
        }
        return {};
    }
};
```

### Example 2

- code

```markdown
{{</* highlight cpp "linenos=table, linenostart=25, hl_lines=4 6-10" */>}}
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> hashtable;
        for (int i = 0; i < nums.size(); ++i) {
            auto it = hashtable.find(target - nums[i]);
            if (it != hashtable.end()) {
                return {it->second, i};
            }
            hashtable[nums[i]] = i;
        }
        return {};
    }
};
{{</* /highlight */>}}
```

- result

{{< highlight cpp "linenos=table, linenostart=25, hl_lines=4 6-10" >}}
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> hashtable;
        for (int i = 0; i < nums.size(); ++i) {
            auto it = hashtable.find(target - nums[i]);
            if (it != hashtable.end()) {
                return {it->second, i};
            }
            hashtable[nums[i]] = i;
        }
        return {};
    }
};
{{< /highlight >}}

### Example 3

- code

````markdown
```python {linenos=true, anchorlinenos=1, lineanchors="anchor"}
print("Hello World")
```
````

- result

```python {linenos=true, anchorlinenos=1, lineanchors="anchor"}
print("Hello World")
```

### Example 4

````markdown
```python {linenos=false}
print("Hello World")
```
````

- result

```python {linenos=false}
print("Hello World")
```

<br>

## Languages

- Bash: `bash`, `sh`, `ksh`, `zsh`, `shell`
- C: `c`
- C#: `csharp`, `c#`
- C++: `cpp`, `c++`
- CMake: `cmake`
- CSS: `css`
- Docker: `docker`, `dockerfile`
- Go: `go`, `golang`
- HTML: `html`
- Java: `java`
- JavaScript: `js`, `javascript`
- JSON: `json`
- Kotlin: `kotlin`
- Lua: `lua`
- Makefile: `make`, `makefile`, `mf`, `bsdmake`
- Markdown: `md`, `mkd`
- Objective-C: `objective-c`, `objectivec`, `obj-c`, `objc`
- Txt: `text`, `plain`, `no-highlight`
- PowerShell: `powershell`, `posh`, `ps1`, `psm1`, `psd1`, `pwsh`
- Protocol Buffer: `protobuf`, `proto`
- Python3: `python`, `py`, `sage`, `python3`, `py3`
- Python2: `python2`, `py2`
- R: `splus`, `s`, `r`
- Ruby: `rb`, `ruby`, `duby`
- Rust: `rust`, `rs`
- Sass: `sass`
- Scala: `scala`
- SQL: `sql`
- Swift: `swift`
- TeX: `tex`, `latex`
- TOML: `toml`
- TypeScript: `ts`, `tsx`, `typescript`
- XML: `xml`
- YAML: `yaml`

<br>

## References

1. [Syntax highlighting | Hugo](https://gohugo.io/content-management/syntax-highlighting/)
