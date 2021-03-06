---
tags: [filesystem, linux, osx]
title: ls
created: '2019-07-30T06:19:49.165Z'
modified: '2020-01-14T04:51:45.259Z'
---

# ls

> list directory contents

## usage
```sh
ls -1                             # force output to be one entry per line.

ls -i                             # print each file's inode number

ls -A                             # list all entries except for . and ..

ls -d .*	                        # list only .dotfiles and .dotdirs

ls -d */                          # only directories

ls -r                             # reverse sort

ls -S                             # sort by size

ls -t                             # sort by date

ls -Z, --context                  # security context so it fits on most displays. Displays only mode, user, group, security context and file name.
                                  # aka "SELinux context"

ls -l | grep "^d"                 # list only directories

ls -l --ignore=*.gz --ignore=*.1  # ignore extensions

ls -l                             # prints file-mode, which consists of entry-type, owner-permissions, and group-permissions
#   d rwx r-x r-x ..
#   ┬
#  entry type character describes the type of file:
#    b     Block special file
#    c     Character special file
#    d     Directory
#    l     Symbolic link
#    s     Socket link
#    p     FIFO
#    -     Regular file
```

## see also
- [[lsattr]]
- [[chmod]]
- [[df]]
- [[find]]
- [[tree]]
- [[stat]]
