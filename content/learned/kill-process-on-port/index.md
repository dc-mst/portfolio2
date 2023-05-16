---
title: Kill a process running on port x on Linux
summary: Killing a ghost process
date: 2023-05-16
lastmod: 2023-05-16
tags: [ BASH ]
---

```bash
sudo kill -9 `sudo lsof -t -i:[x]`
```

where `[x]` is the port number
