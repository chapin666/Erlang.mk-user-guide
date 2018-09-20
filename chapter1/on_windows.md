## 1.2. On Windows

Erlang.mk 可以在安装了 MSYS2 环境的 Windows 上使用。 目前不支持Cygwin，MSYS（原始）和本机Windows（Batch和PowerShell）。

> Note

> Erlang.mk 期望在大多数文件中使用 Unix 换行符（LF 而不是 CRLF）。 确保充分配置文本编辑器。

> 本节的其余部分详细介绍了如何设置 Erlang/OTP 和 MSYS2 以便使用 Erlang.mk。

### 1.2.1. 安装 Erlang/OTP

Erlang.mk 需要安装 Erlang/OTP。 OTP 团队为[官方下载](http://www.erlang.org/downloads)页面提供所有主要和次要版本的 Erlang/OTP 二进制文件。 除非技术上不可行，否则建议您使用64位安装程序。 请按照安装程序中的说明完成安装。

如果您需要其他参考，OTP 团队还提供了在 [Windows 上安装 Erlang/OTP](http://www.erlang.org/downloads) 的简短指南。

您可以使用命令行上的 /S开关静默安装 Erlang/OTP：
```
C:\Users\essen\Downloads> otp_win64_18.0.exe /S
```
### 1.2.2. 安装 MSYS2

Windows 上唯一受支持的环境是 MSYS2。 MSYS2 是一个类似于 Windows 的轻量级 Unix 环境，它与 Arch Linux 软件包管理器 pacman 一起提供。

MSYS2 项目提供了一键安装程序和安装后设置的说明。

目前无法以静默方式使用安装程序。 值得庆幸的是，MSYS2 项目提供了一个可用于代替安装程序的压缩包。 但是归档需要 7zip 来解压缩它。

首先，下载 MSYS2基本压缩包并在 C:\ 下解压缩。 假设您将存档下载为 msys2.tar.xz 并将其放在 C:\ 中，您可以使用以下命令将其解压缩：
```
C:\> 7z x msys2.tar.xz
C:\> 7z x msys2.tar > NUL
```
然后，您可以运行执行安装后设置所需的两个命令：
```
C:\> C:\msys64\usr\bin\bash -lc "pacman --needed --noconfirm -Sy bash pacman pacman-mirrors msys2-runtime"

C:\> C:\msys64\usr\bin\bash -lc "pacman --noconfirm -Syu"
```

### 1.2.3. 安装所需的MSYS2包

按照这些说明操作后，您可以安装 GNU Make ， Git 和任何其他所需的软件。 从 MSYS2 shell，您可以直接调用 pacman：
```
$ pacman -S git make
```
您可以使用 pacman -Ss 来搜索包。 例如，要查找与 GCC 相关的所有包：
```
$ pacman -Ss gcc
```
如果您要编译 C/C++ 代码，则需要安装此软件包，因为 Erlang.mk 无法使用默认的 “gcc” 软件包：
```
$ pacman -S mingw-w64-x86_64-gcc
```
您还可以从 Windows 命令行或 MSYS2环境下运行命令。 这个命令将安装 GNU Make 和 Git：
```
C:\> C:\msys64\usr\bin\bash -lc "pacman --noconfirm -S git make"
```
如果从 MSYS2 环境中运行程序，则可以使用类似的 bash 命令。

###  1.2.4. 陷阱

虽然大多数基本功能都可以使用，但仍然存在一些问题。 在运行 Erlang 脚本时，需要修复  Erlang.mk 以传递正确的路径。 我们正在做这件事。 Erlang.mk 在 Linux 和 Windows 上都经过了全面测试，但是在本指南尚未涉及的领域缺乏测试，因此随着更多测试的增加，需要修复错误。