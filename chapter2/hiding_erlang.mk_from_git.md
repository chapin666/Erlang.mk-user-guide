## 在 git 中隐藏 Erlang.mk

Erlang.mk 是一个大文本文件。 它可以轻松地占用 git diff 或 git grep 命令的很大一部分。 你可以通过告诉 Git erlang.mk 是一个二进制文件来避免这种情况。

将其添加到 .gitattributes 文件中。 这是您可以在仓库的根目录中创建的文件：
```
erlang.mk -diff
```
erlang.mk 文件仍将出现在 diff 和 greps 中，但作为二进制文件，意味着其内容将不再默认显示。