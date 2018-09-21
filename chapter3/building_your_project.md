## 构建你的项目

Erlang.mk 是一个构建工具。 它专为 Erlang 开发人员量身定制，并在 Erlang 社区中广泛实践。

Erlang.mk 很乐意构建您抛出的所有 [Erlang 特定文件](https://erlang.mk/guide/building.html)。 其他类型的文件，例如在处理 NIF 或端口驱动程序时使用 [C 或 C++ 代码](https://erlang.mk/guide/ports.html)。

Erlang.mk 包含[源依赖](https://erlang.mk/guide/deps.html)的概念。 它可以使用各种机制获取依赖源代码，包括从 Git，Mercurial 或 SVN 获取。

Erlang.mk 将在适用时自动[生成版本](https://erlang.mk/guide/relx.html)。 它还可以[生成脚本](https://erlang.mk/guide/escript.html)。