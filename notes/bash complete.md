---
tags: [bash/built-in]
title: bash complete
created: '2019-07-30T06:19:48.994Z'
modified: '2020-01-10T10:17:09.126Z'
---

# bash complete

## usage
```sh
complete -W "word1 word2 .." command    # -W wordlist provide a list of words for completion


complete -A directory dothis           # only directory names



_dothis_completions() {
  COMPREPLY+=("now")                   # array variable used to store the completions        
  COMPREPLY+=("tomorrow")
  COMPREPLY+=("never")
}

complete -F _dothis_completions dothis    # -F flag defining function that will provide the completions
```

## see also
- [Creating a bash completion script](https://iridakos.com/tutorials/2018/03/01/bash-programmable-completion-tutorial.html)
