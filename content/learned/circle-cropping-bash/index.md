---
title: Circular cropping from BASH
summary: Circular crop without opening any app...
date: 2023-05-12
lastmod: 2023-05-12
tags: [ Linux, BASH ]
---

The drawing should be ~ half of the original image

```bash
convert input.png \
        -gravity Center \
        \( -size 1024x1024 \
           xc:Black \
           -fill White \
           -draw 'circle 500 500 500 1' \
           -alpha Copy \
        \) -compose CopyOpacity -composite \
        -trim output.png
```


