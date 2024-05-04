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

## What is front matter?

Front matter is metadata placed at the top of each content file in a format that Hugo can understand. It typically includes information such as the title, date, author, and other metadata relevant to the content of the file. Hugo uses front matter to determine how to process and display the content within the file.

Example:

```markdown
---
title: "My First Post"
date: "2024-05-04T19:53:57+08:00"
draft: true
---
```

## Why use front matter?

- Describes the content
- Augments the content
- Establishes relationships with other content
- Controls the published structure of your site
- Determines template selection

## Front matter types

Front matter in archetype files (`/archetypes/*`) is go template.

```markdown
---
title: '{{ replace .File.ContentBaseName `-` ` ` | title }}'
date: '{{ .Date }}'
draft: true
---
```

Front matter in content files (`/content/*`) is specific content.

```markdown
---
title: "My First Post"
date: "2024-05-04T19:53:57+08:00"
draft: true
---
```

## How to configure front matter?

### Template

More archetypes content refers to [Hugo Archetypes](hugo-archetypes.md).

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

### Specific

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

### Theme Everest template config

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
