---
title: Modified grep command
summary: a grep command with auto-hiding capabilities
date: 2023-05-10
lastmod: 2023-05-10
tags: [ Linux, BASH ]
---

When executing the command `ps aux | grep -rI process`, the displayed results appear as follows:

```bash
  8176  process
  8189  grep -rI process
```

The second entry in the result corresponds to the command we just executed. Although this is typically not problematic, it can lead to issues if you intend to use this command within a bash if statement to check whether `process` is running. In such cases, the command would return true even if `process` is not running.

To ensure that the command returns nothing when `process` is not running, you can modify it as follows:

```bash
ps aux | grep -rI [p]rocess
```

The addition of brackets in the regex causes grep to interpret the query in the same way, but it prevents the literal string `[p]rocess` from matching `process_name`. Consequently, the modified command produces the following desired output:

```bash
8176  process
```

This behavior is preferable for certain use cases.

