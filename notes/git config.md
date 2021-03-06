---
tags: [git, heredoc]
title: git config
created: '2019-08-01T07:03:58.247Z'
modified: '2019-11-29T11:39:16.590Z'
---

# git config

## usage
```sh
git config --global user.name "Your Name"         # Set the name that will be attached to your commits and tags.

git config --global user.email "you@example.com"  # Set the e-mail address that will be attached to your commits and tags.

git config --global color.ui auto                 # Enable some colorization of Git output. 

git config --list [--local|--global]              # list local/global configuration
```

## seperate configs per remote
```sh
cat <<EOF > ~/.gitconfig
[core]
  editor = vim

[includeIf "gitdir:~/gitlab.com/"]
  path = ~/.gitconfig-gitlab

[includeIf "gitdir:~/github.com/"]
  path = ~/.gitconfig-github
EOF


cat <<EOF > ~/.gitconfig-github
[user]
  name  = user
  email = user@mail.com

[push]
  default = simple
EOF
```

## see also
- [[git]]
