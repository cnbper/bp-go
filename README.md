# GO

<https://golang.google.cn>

## 配置环境变量

```shell
$ vi ~/.bash_profile
export GOROOT=/Users/zhangbaohao/software/golang/go
export GOPATH=/Users/zhangbaohao/software/golang/workspace
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin

$ source ~/.bash_profile

$ go version
```

## 设置终端代理

```shell
export http_proxy="http://127.0.0.1:1087/"
export https_proxy="http://127.0.0.1:1087/"

curl www.google.com
curl https://go.googlesource.com/tools/
```

## 设置Sourcetree代理

仓库 > 仓库设置 > 远程仓库 > 编辑配置文件

```conf
[http]
    proxy = 127.0.0.1:1087
```

## 设置docker代理

preferences > Proxies

## 安装依赖管理工具dep

```shell
# 安装官方依赖管理工具dep
$ go get -u github.com/golang/dep/cmd/dep

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

## 依赖管理工具go mod

```shell
# 下载依赖到$GOPATH/pkg/mod
GO111MODULE=on go mod download
```