## 使用 templates

众所周知，Erlang 的 OTP 行为往往会有一些模板。 除了创建新模块之外，它当然很少成为问题。 这就是为什么 Erlang.mk 不仅带有用于生成项目的模板，还有单独的 modules！

您可以使用 list-templates 目标列出所有可用模板：
```
$ make list-templates
Available templates:
  cowboy_http
  cowboy_loop
  cowboy_rest
  cowboy_ws
  gen_fsm
  gen_server
  gen_statem
  ranch_protocol
  supervisor
```
要生成一个模块，我们把它称之为 gen_server，你需要做的就是使用适当的参数调用make new：
```
$ make new t=gen_server n=my_server
```
这将使用 gen_server 模板在 src/my_server.erl 中创建 module。

下次运行 make 时会自动编译该模块：
```
$ make
 ERLC   my_server.erl
 APP    hello_joe.app.src
```
剩下要做的就是在你喜欢的编辑器中打开它并让它做点什么！