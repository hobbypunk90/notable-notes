---
tags: [bash]
title: tee
created: '2019-07-30T06:19:49.251Z'
modified: '2019-07-30T07:06:01.899Z'
---

# tee


### redirecting from tee to multiple files
```sh
vault write -format=json pki/root/generate/internal common_name="pki-ca-root" ttl=87600h \
   | tee \
  >(jq -r .data.certificate > ca.pem) \
  >(jq -r .data.issuing_ca > issuing_ca.pem) \
  >(jq -r .data.private_key > ca-key.pem)
```