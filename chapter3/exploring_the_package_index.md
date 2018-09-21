## 探索包索引

Erlang.mk [内置包索引](https://erlang.mk/guide/deps.html)。 它构建为依赖系统的扩展，旨在用于发现目的。

没有安装任何软件包，它们仅用作依赖项，并且始终是项目特定的。 可以将它们视为普通依赖项的快捷方式。

您可以使用搜索目标获取 Erlang.mk 已知的所有包的列表：
```
$ make search
```
您还可以使用此目标搜索所有包，例如查找与 Cowboy 相关的所有包：
```
$ make search q=Cowboy
```