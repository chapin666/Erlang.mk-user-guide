## 4.3. 自定义构建

Erlang.mk 允许您自定义哪些组件包含在 erlang.mk 文件中。 WITHOUT 变量允许您从默认的 Erlang.mk 构建中删除组件。 build.config 文件允许您准确定义内容（包括您自己的代码！），以及按什么顺序。

WITHOUT 文件包含要从构建中排除的组件列表。 例如，要在引导应用程序时排除包索引和 EDoc 插件：
```
$ make -f erlang.mk bootstrap WITHOUT="index plugins/edoc"
```
生成的 Erlang.mk 在更新时永远不会包含这些组件，直到您改变主意并在升级时再次使用 WITHOUT 变量：
```
$ make erlang-mk WITHOUT=index
```
当您引导 Erlang.mk 或使用 make erlang-mk 更新它时，将自动使用 build.config 文件。

build.config 文件包含将要生成的 erlang.mk 文件中构建的所有文件的列表。 您可以从[最新版本](https://github.com/ninenines/erlang.mk/blob/master/build.config)开始，并根据您的需求进行自定义。

您还可以通过修改 ERLANG_MK_BUILD_CONFIG 的值，以不同方式命名文件或将其放在单独的文件夹中。 您还可以通过更改 ERLANG_MK_BUILD_DIR 变量来告诉 Erlang.mk 使用不同的临时目录。

如果要使用其他仓库或特定提交进行更新，可以使用变量 ERLANG_MK_REPO 和 ERLANG_MK_COMMIT。