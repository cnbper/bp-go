# 代理配置

## 设置终端代理

```shell
export http_proxy="http://127.0.0.1:1087/"
export https_proxy="http://127.0.0.1:1087/"

# 测试
curl www.google.com
curl https://go.googlesource.com/tools/
```

## 设置Sourcetree代理

- 仓库 > 仓库设置 > 远程仓库 > 编辑配置文件

```conf
[http]
    proxy = 127.0.0.1:1087
```

## 设置docker代理

preferences > Proxies