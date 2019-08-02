---
tags: [bash]
title: parallel gnu
created: '2019-07-30T06:19:49.203Z'
modified: '2019-07-30T08:10:06.742Z'
---

# parallel gnu


```sh
parallel --eta -j8 ./parallel_check-short-links.sh {} :::: ./foo.csv

# --bar


tail -n +266300 ./OTSDE/shortener_OTSDE_YESPPYESPM_OK.txt.csv | \
  parallel --eta ./parallel_check-short-links.sh {}

```