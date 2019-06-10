# dep

## 安装

```shell
# 安装官方依赖管理工具dep
$ go get -u github.com/golang/dep/cmd/dep
```

## 初始化

```shell
# 初始化项目
$ dep init
$ ls
Gopkg.lock      Gopkg.toml      vendor
# 添加依赖
$ dep ensure -add github.com/pkg/errors

# 升级某个依赖项目的版本，需要修改Gopkg.toml
$ dep ensure -update xxxx

# 执行"go build .."时会自动优先从vendor目录中寻找依赖项的源代码
```
