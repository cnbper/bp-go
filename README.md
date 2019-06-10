# GO

<https://golang.google.cn>

## 配置GO开发环境

```shell
# 安装
$ rm -rf /Users/zhangbaohao/software/golang/go
$ tar -C /Users/zhangbaohao/software/golang -xzf go1.12.5.darwin-amd64.tar.gz

# 配置环境变量
$ vi ~/.bash_profile
export GOROOT=/Users/zhangbaohao/software/golang/go
export GOPATH=/Users/zhangbaohao/software/golang/workspace
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
$ source ~/.bash_profile

# 获取版本信息
$ go version
```
