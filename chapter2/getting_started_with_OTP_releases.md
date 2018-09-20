## 2.5. OTP releases 入门

OTP 版本是 Erlang RunTime 系统（ERTS）与您的节点需要运行的所有库和文件的组合。 它完全独立，通常可以按原样发送到您的生产系统，无需任何额外设置即可运行。

Erlang.mk 可以引导你的项目来生成版本。 您可以使用 bootstrap-rel 来实现此目的：
```
$ make bootstrap-rel
```
此目标可以与bootstrap或bootstrap-lib结合使用，以创建将构建版本的项目：
```
$ make -f erlang.mk bootstrap-lib bootstrap-rel
```

在操作期间保持命令的顶级项目非常有用，并将系统的组件放在您将依赖的单独应用程序中。 有关更多信息，请参阅[包和依赖项](https://erlang.mk/guide/deps.html)章节。

从现在开始运行 make 时，Erlang.mk 将编译您的项目并构建版本
```
$ make
 APP    hello_joe.app.src
 GEN    distclean-relx-rel
 GEN    /home/essen/tmp/hello_joe/relx
===> Starting relx build process ...
===> Resolving OTP Applications from directories:
          /home/essen/tmp/hello_joe/ebin
          /usr/lib/erlang/lib
          /home/essen/tmp/hello_joe/deps
===> Resolved hello_joe_release-1
===> Including Erts from /usr/lib/erlang
===> release successfully created!
```
第一次运行此命令时，Erlang.mk 将下载 relx，即发布构建工具。 所以如果你看到比上面更多的输出，不要担心。

如果构建版本很慢，则无需升级硬件。 有关加速开发期间构建时间的各种提示，请参阅“[Releases](https://erlang.mk/guide/relx.html)”一章。

您可以使用 ./_rel/hello_joe_release/bin/hello_joe_release 脚本启动发行版，或者只运行 make run。 后者还将编译您的项目并构建发布：
```
$ make run
 APP    hello_joe.app.src
 GEN    distclean-relx-rel
===> Starting relx build process ...
===> Resolving OTP Applications from directories:
          /home/essen/tmp/hello_joe/ebin
          /usr/lib/erlang/lib
          /home/essen/tmp/hello_joe/deps
===> Resolved hello_joe_release-1
===> Including Erts from /usr/lib/erlang
===> release successfully created!
Exec: /home/essen/tmp/hello_joe/_rel/hello_joe_release/erts-7.0/bin/erlexec -boot /home/essen/tmp/hello_joe/_rel/hello_joe_release/releases/1/hello_joe_release -boot_var ERTS_LIB_DIR /home/essen/tmp/hello_joe/_rel/hello_joe_release/erts-7.0/../lib -env ERL_LIBS /home/essen/tmp/hello_joe/_rel/hello_joe_release/releases/1/lib -config /home/essen/tmp/hello_joe/_rel/hello_joe_release/releases/1/sys.config -args_file /home/essen/tmp/hello_joe/_rel/hello_joe_release/releases/1/vm.args -- console
Root: /home/essen/tmp/hello_joe/_rel/hello_joe_release
/home/essen/tmp/hello_joe/_rel/hello_joe_release
heart_beat_kill_pid = 16389
Erlang/OTP 18 [erts-7.0] [source] [64-bit] [smp:4:4] [async-threads:10] [hipe] [kernel-poll:false]

Eshell V7.0  (abort with ^G)
(hello_joe@127.0.0.1)1>
```
Simple as that!


