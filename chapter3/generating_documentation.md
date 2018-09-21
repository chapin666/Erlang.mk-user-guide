## 文档生成

Erlang.mk 支持 EDoc 和 Asciidoc。

[EDoc](https://erlang.mk/guide/edoc.html) 直接从您的源代码生成 HTML 文档。

虽然很方便，但问问自己：如果所有文档都在源代码中，为什么不直接打开源代码？ 这就是 Asciidoc 来源的目的。

[Asciidoc](https://erlang.mk/guide/asciidoc.html) 插件希望所有文档都与源代码分开。 它将从仓库的 doc/src/ 文件夹中编写的文档生成 HTML，PDF，手册页等。