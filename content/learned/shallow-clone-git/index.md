---
title: Shallow clone with Git
summary: Only check the lastest states
date: 2023-05-19
lastmod: 2023-05-19
tags: [ Git ]
---

If you only want to check the latest states, without downloading anything:

```bash
git clone -–depth <depth in numbers> <url>

```

Also for a single branch:

```bash
git clone <url> --branch <branch-to-clone> --single-branch [folder-to-store]
```