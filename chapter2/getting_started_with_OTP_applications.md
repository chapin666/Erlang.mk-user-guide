## 2.3. OTP application 入门

OTP 应用程序是具有监督树的 Erlang 应用程序。 换句话说，它将始终运行进程。

这种项目可以由 Erlang.mk 自动生成。 您需要做的就是使用 bootstrap：
```
$ make -f erlang.mk bootstrap
```
然后会在屏幕上显示类似于以下代码段的内容：
```
git clone https://github.com/ninenines/erlang.mk .erlang.mk.build
Cloning into '.erlang.mk.build'...
remote: Counting objects: 4035, done.
remote: Compressing objects: 100% (12/12), done.
remote: Total 4035 (delta 8), reused 4 (delta 4), pack-reused 4019
Receiving objects: 100% (4035/4035), 1.10 MiB | 784.00 KiB/s, done.
Resolving deltas: 100% (2442/2442), done.
Checking connectivity... done.
if [ -f build.config ]; then cp build.config .erlang.mk.build; fi
cd .erlang.mk.build && make
make[1]: Entering directory '/home/essen/tmp/hello_joe/.erlang.mk.build'
awk 'FNR==1 && NR!=1{print ""}1' core/core.mk index/*.mk core/index.mk core/deps.mk plugins/protobuffs.mk core/erlc.mk core/docs.mk core/test.mk plugins/asciidoc.mk plugins/bootstrap.mk plugins/c_src.mk plugins/ci.mk plugins/ct.mk plugins/dialyzer.mk plugins/edoc.mk plugins/elvis.mk plugins/erlydtl.mk plugins/escript.mk plugins/eunit.mk plugins/relx.mk plugins/shell.mk plugins/triq.mk plugins/xref.mk plugins/cover.mk \
    | sed 's/^ERLANG_MK_VERSION = .*/ERLANG_MK_VERSION = 1.2.0-642-gccd2b9f/' > erlang.mk
make[1]: Leaving directory '/home/essen/tmp/hello_joe/.erlang.mk.build'
cp .erlang.mk.build/erlang.mk ./erlang.mk
rm -rf .erlang.mk.build
```

这是Erlang.mk引导自身。 实际上，您最初下载的文件只包含引导程序所需的代码。 此操作仅执行一次。 有关更多信息，请参阅[更新Erlang.mk](https://erlang.mk/guide/updating.html)章节。

当然，现在可以编译生成的项目：
```
$ make
```
Cheers!
