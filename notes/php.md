---
tags: [lang, lang/php]
title: php
created: '2019-07-30T06:19:49.206Z'
modified: '2019-08-02T07:19:54.381Z'
---

# php

```sh
php -i 

php -a # start php repl

php -r # exec php code in oneline
```
### inline
```sh
php -r \'echo gethostbyname("foo.bar.domain.net").PHP_EOL; echo "---".PHP_EOL; foreach(dns_get_record("foo.bar.domain.net", DNS_A) as $i){ echo $i["ip"].PHP_EOL;};\'
```