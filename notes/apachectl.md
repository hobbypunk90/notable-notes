---
tags: [linux]
title: apachectl
created: '2019-11-28T11:55:25.653Z'
modified: '2019-12-26T19:37:40.377Z'
---

# apachectl

## usage
```sh
apachectl configtest                # test config

/usr/local/apache/bin/apachectl configtest


apache2ctl -M                     # list loaded modules

apachectl -t -D DUMP_MODULES      # list loaded modules

ls /etc/apache2/mods-enabled/		  # list enabled modules
ls /etc/apache2/mods-available/		# list available modules
```

## see also
- [[apache2]]
