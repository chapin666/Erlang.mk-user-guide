## 从 scratch 开始

如果您已有应用程序，或者想要完全控制将创建哪些文件，则可以手动设置 Erlang.mk。

Erlang.mk很容易设置：您需要做的就是创建一个文件夹，将 Erlang.mk 放入其中，然后编写一行 Makefile，其中包含：
```
include erlang.mk
```
详细步骤：
```
$ mkdir hello_joe
$ cd hello_joe
$ curl https://erlang.mk/erlang.mk -o erlang.mk
$ echo "include erlang.mk" > Makefile
$ make
```
从这开始，您可以创建一个src/文件夹或开始使用模板。