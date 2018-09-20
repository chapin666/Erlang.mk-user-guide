### 获取帮助

在开发过程中，如果您不记得目标的名称，可以随时运行make help：
```
$ make help
erlang.mk (version 1.2.0-642-gccd2b9f) is distributed under the terms of the ISC License.
Copyright (c) 2013-2016 Loïc Hoguin <essen@ninenines.eu>

Usage: [V=1] make [target]...

Core targets:
  all           Run deps, app and rel targets in that order
  app           Compile the project
  deps          Fetch dependencies (if needed) and compile them
  search q=...  Search for a package in the built-in index
  rel           Build a release for this project, if applicable
  docs          Build the documentation for this project
  install-docs  Install the man pages for this project
  check         Compile and run all tests and analysis for this project
  tests         Run the tests for this project
  clean         Delete temporary and output files from most targets
  distclean     Delete all temporary and output files
  help          Display this help and exit
  erlang-mk     Update erlang.mk to the latest version

Bootstrap targets:
  bootstrap          Generate a skeleton of an OTP application
  bootstrap-lib      Generate a skeleton of an OTP library
  bootstrap-rel      Generate the files needed to build a release
  new t=TPL n=NAME   Generate a module NAME based on the template TPL
  list-templates     List available templates
....
```

本指南应提供任何解答。 如果没有，请在[官方仓库](https://github.com/ninenines/erlang.mk/issues)上打开一个 ticket，我们将努力改进指南。

Nine Nines 提供商业支持。 请发送电子邮件至 contact@ninenines.eu 联系 LoïcHoguin。