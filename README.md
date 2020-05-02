# go-gin-admin
Backend Admin API based on GO+GIN

## Create Application
```bash
$ mkdir go-gin-admin && cd go-gin-admin

$ go env -w GO111MODULE=on

$ go env -w GOPROXY=https://goproxy.cn,direct

$ go mod init github.com/SmartNMS/go-gin-admin
go: creating new go.mod: module github.com/SmartNMS/go-gin-admin

$ ls
go.mod
```

## Install GIN Module
```bash
go get -u github.com/gin-gonic/gin
```

## Update Dependency
```bash
go mod tidy
```

## Create Application Directory Structure
```
go-gin-admin/
├── conf
├── middleware
├── models
├── pkg
├── routers
└── runtime
```

## Add Go Modules Replace

- go.mod

```txt
require (...)

replace (
		github.com/SmartNMS/go-gin-admin/pkg/setting => ~/go/src/go-gin-admin/pkg/setting
		github.com/SmartNMS/go-gin-admin/conf    	  => ~/go/src/go-gin-admin/pkg/conf
		github.com/SmartNMS/go-gin-admin/middleware  => ~/go/src/go-gin-admin/middleware
		github.com/SmartNMS/go-gin-admin/models 	  => ~/go/src/go-gin-admin/models
		github.com/SmartNMS/go-gin-admin/routers 	  => ~/go/src/go-gin-admin/routers
)
```

## Reference

https://eddycjy.com/posts/go/gin/2018-02-10-install/

