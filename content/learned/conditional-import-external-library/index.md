---
title: Python conditional import in external library
summary: how to import in an external library
date: 2022-05-11
lastmod: 2023-05-11
tags: [ Python ]
---

```python
from logging import getLogger
import foo

try:
    import bar as br
    BAR_INSTALLED = True
    msg = "bar is imported."
except ImportError:
    BAR_INSTALLED = False
    msg = "bar is not available."


logger = getLogger(__main__)
logger.info(msg)
```
