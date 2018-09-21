## 5.1. Erlang必须可用

当前 Erlang.mk 要求您事先安装 Erlang。 安装 Erlang 并不总是很容易，特别是如果您需要针对特定项目的特定版本的 Erlang。

另外，在使用 Erlang.mk 之前，使用的 Erlang 必须在 $PATH 中。

在未来我们设想，Erlang.mk 可以管理您使用项目所需的 Erlang版本。 Erlang.mk 已经在使用 make ci 时运行测试，因此在开发过程中执行此操作只需一步之遥。