---
title: "Forks"
date: "2014-08-02"
groups: ['nlgd']
groups_weight: 10
---

[Conformal](https://conformal.com/) created and maintains [Go](http://golang.org) packages implementing bitcoin. These [packages](https://github.com/conformal/?query=btc) are [forked](https://github.com/nlgcoin/?query=nlg) and changed to fit the Guldencoin project.

Read about btcd project at conformal's blog: [https://blog.conformal.com/category/btcd/](https://blog.conformal.com/category/btcd/).

## Goal

The goal of the nlg forks is to provide nlg-compatible Go packages and commands, while tracking upstream for changes.

## Changes

Several changes are made to the Guldencoin versions of the btc* packages.

### Credits
Adding following notice to the README.md files of forked repo's:

```
### Credits

This repository is forked from [conformal/<btc*>](https://github.com/conformal/<btc*>) and changed to work with the Guldencoin network.
```

### Branding
Find/replace's in documentation and code:

 - 'btc' > 'nlg'
 - 'bitcoin' > 'guldencoin'

### Scrypt
TODO: Some information about script.

### KGW
TODO: Some information about KGW.

## Upstream tracking

The upstream changes are merged down regularly.
When we fix or add something that we think could be a benefit for the btc* project, we will create a pull request containing the additions at their repo.

## Package list
These are the packages that are forked and the package that they're forked from:

 - [nlgec](https://github.com/nlgcoin/nlgec) (forked from [btcec](https://github.com/conformal/btcec))


