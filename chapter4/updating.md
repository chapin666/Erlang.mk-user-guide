## 4.2. 更新

后来，更新成为必需品。 Erlang.mk 开发人员和贡献者不懈地改进项目并添加新功能; 如果不从中受益将是一种浪费。

这就是更新 Erlang.mk 如此简单的原因。 您需要做的就是调用 make erlang-mk：
```
$ make erlang-mk
git clone https://github.com/ninenines/erlang.mk .erlang.mk.build
Cloning into '.erlang.mk.build'...
remote: Counting objects: 4035, done.
remote: Compressing objects: 100% (12/12), done.
remote: Total 4035 (delta 8), reused 4 (delta 4), pack-reused 4019
Receiving objects: 100% (4035/4035), 1.10 MiB | 1000.00 KiB/s, done.
Resolving deltas: 100% (2442/2442), done.
Checking connectivity... done.
if [ -f build.config ]; then cp build.config .erlang.mk.build; fi
cd .erlang.mk.build && make
make[1]: Entering directory '/home/essen/tmp/emkg/hello_joe/.erlang.mk.build'
awk 'FNR==1 && NR!=1{print ""}1' core/core.mk index/*.mk core/index.mk core/deps.mk plugins/protobuffs.mk core/erlc.mk core/docs.mk core/test.mk plugins/asciidoc.mk plugins/bootstrap.mk plugins/c_src.mk plugins/ci.mk plugins/ct.mk plugins/dialyzer.mk plugins/edoc.mk plugins/elvis.mk plugins/erlydtl.mk plugins/escript.mk plugins/eunit.mk plugins/relx.mk plugins/shell.mk plugins/triq.mk plugins/xref.mk plugins/cover.mk \
    | sed 's/^ERLANG_MK_VERSION = .*/ERLANG_MK_VERSION = 1.2.0-642-gccd2b9f/' > erlang.mk
make[1]: Leaving directory '/home/essen/tmp/emkg/hello_joe/.erlang.mk.build'
cp .erlang.mk.build/erlang.mk ./erlang.mk
rm -rf .erlang.mk.build
```
剩下要做的就是提交文件！

是的，就这么简单。