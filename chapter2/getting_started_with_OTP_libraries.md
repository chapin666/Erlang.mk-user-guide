## OTP libraries 入门

OTP库 是一个没有监督树的 Erlang 应用程序。 换句话说，它只不过是模块。

这种项目也可以由 Erlang.mk 使用 bootstrap-lib 生成：
```
$ make -f erlang.mk bootstrap-lib
```
Erlang.mk 将再次自我引导并为您的项目生成所有文件。 你现在可以编译它：
```
$ make
```
Enjoy!