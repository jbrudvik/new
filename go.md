# New [Go](https://go.dev) project

## Create new Go module

```sh
$ MODPATH="github.com/user/repo"
$ MODBASE=$(basename $MODPATH)

$ mkdir $MODBASE
$ cd $MODBASE
$ go mod init $MODPATH
$ echo 'package main\nimport "fmt"\nfunc main() {\nfmt.Println("hello, world!")\n}' > main.go && go fmt
$ echo $MODBASE > .gitignore

$ go run .
```

## ...as a new Git repo

```sh
$ git init
$ git add .
$ git commit -m "Initial commit"
```

## ...on GitHub

```sh
$ gh repo create $MODBASE --private --source=.
$ git push
```
