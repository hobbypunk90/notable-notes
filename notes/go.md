---
tags: [go]
title: go
created: '2019-07-30T06:19:49.075Z'
modified: '2019-08-22T15:00:29.104Z'
---

# go

```
  has                             doesn't have

+ package system                - implicit numeric conversion
+ first-class-functions         - constructors/destructors
+ lexical-scope                 - operator overloading
+ system call interface         - default parameter values
+ immutable string in utf-8     - inheritance (type-based inheritance → subclasses)
+ struct ~ class                - generics    `parametrics polimorphism` ≈ `generics`
+ concurrency support (CSP)     - exceptions
                                - macros
+ `garbage collected`           - function annotations
+ it's `staticallly typed`      - thread local storage
                                - inheritance but composition of type
                                - explicit declaration, interface-implementation required
```

## semicolon rule

> `;` terminates statements

if last token before new line:
- is an `identifiere`   -> `int`, `float64`
- is an `basic literal` -> `number`, `string`
- is a `token`          -> `break`, `continues`, `fallthrough`, `return`, `++`, `--`, `)`, `}`

if the new line comes after a `token` that could end the statement => insert `;`

## see also
- [[go help]]
- [[go build]]
- [[go install]]
- [[go test]]
- [[go run]]
