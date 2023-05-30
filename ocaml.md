# New [OCaml](https://ocaml.org) project

## Create new OCaml project

```sh
$ PROJECT=<project-name>

$ dune init project $PROJECT
$ cd $PROJECT
$ dune build
$ echo _build > .gitignore
$ dune exec $PROJECT
```

## ...as a new Git repo

```sh
$ git init
$ git add .
$ git commit -m "Initial commit"
```

## ...on GitHub

```sh
$ gh repo create $PROJECT --private --source=.
$ git push
```
