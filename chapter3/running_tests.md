## 运行测试

Erlang.mk 支持许多不同的测试和静态分析工具。

[make shell](https://erlang.mk/guide/shell.html) 命令允许您手动测试项目。 您可以使用 [EUnit](https://erlang.mk/guide/eunit.html) 自动执行这些单元测试，并使用 [Common Test](https://erlang.mk/guide/ct.html) 测试整个系统。 [代码覆盖](https://erlang.mk/guide/coverage.html)当然可以在测试期间启用。

Erlang.mk 具有在设置和使用[持续集成](https://erlang.mk/guide/ci.html)时让您的生活更轻松的功能。

在静态分析方面，Erlang.mk 支持 [Dialyzer](https://erlang.mk/guide/dialyzer.html) 和 [Xref](https://erlang.mk/guide/xref.html)，以执行成功的类型分析和交叉引用代码。