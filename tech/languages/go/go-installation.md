---
title: Go
page: go
section: tech-languages
order: 1
version: 1.5
---

## Go installation

To install Go compiler, type:

```
$ sudo dnf install go
```

`go` and `gofmt` binaries will become available on the system,
but you will still need to provide `$GOPATH` explicitly.

To set the `$GOPATH` to be your home directory, run:

```
$ echo 'export GOPATH=$HOME' >> $HOME/.profile
$ source $HOME/.profile
```

Run `go env` to check that `$GOPATH` is set correctly:

```
$ go env | grep GOPATH
GOPATH="/home/$USER"
```
