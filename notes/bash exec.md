---
tags: [bash, bash/builtin]
title: bash exec
created: '2019-07-30T06:19:49.006Z'
modified: '2019-07-30T06:23:11.515Z'
---

# bash exec

- replace shell with command
- shell-`PID` == command-`PID`
- `echo $$ == /proc/self`
- spawns new proc

```sh
exec    
```