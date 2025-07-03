# VScode

### brief:

go env -w GO111MODULE="on"


### не дает дебаг - отключить

go: modules disabled by GO111MODULE=off; see 'go help modules'
go env -w GO111MODULE="off"

# import локально и внеш с mod:

без mod - GO111MODULE='off' нельзя включать внешние (github)

- включить
  go env -w GO111MODULE="on"
  go mod init try_sf
  go mod tidy
  go: main imports
  ./drvtest: "./drvtest" is relative, but relative import paths are not supported in module mode
- поправить в import
  dtest "try_sf/drvtest"
- go get github.com/yosuke-furukawa/json5
  go: added github.com/yosuke-furukawa/json5 v0.1.1

при этом в go.mod:

```go
module try_sf

go 1.23.6

require github.com/yosuke-furukawa/json5 v0.1.1 // indirect
```

ок

! go clean -modcache - очистка кеша - приведет к удалению /home/u2610616@corp.mrgeng.ru/go/pkg/

имя пакета должно соответствовать названию директории, в которой расположены его файлы.
К примеру, если в папке application/ содержится файл server.go, то название пакета в нем должно быть package application.

Файлы пакета должны размещаться в одной директоии - иначе не получается

не поможет:
установить в терминале vsc
go env -w GOPATH=$HOME/SVD
go env GOPATH
/home/u2610616@corp.mrgeng.ru/SVD

# не берет import из github

- go env -w GO111MODULE="on"
- go get github.com/yosuke-furukawa/json5/encoding/json5

## Snippets

/home/u2610616@corp.mrgeng.ru/.config/Code/User/snippets/