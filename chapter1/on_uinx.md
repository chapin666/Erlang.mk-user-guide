## 1.1. On Unix

Erlang.mk 需要安装 GNU Make。 虽然它目前适用于 GNU Make 3.81，但对此版本的支持已弃用，将于 2017 年删除。我们建议使用 GNU Make 4.1 或更高版本。

还必须安装 Git 和 Erlang/OTP。

某些功能需要安装 Autoconf 2.59 或更高版本才能编译 Erlang/OTP。 Erlang/OTP 可能会根据您的需求提出进一步的要求。

某些包可能需要其他库。

### 1.1.1. Linux
安装包的命令因发行版而异：

#### Arch Linux
```
$ pacman -S erlang git make
```
Alpine Linux 和其他基于 BusyBox 的发行版都带有一个不兼容的 awk 程序。 需要安装 GNU Awk（在Alpine上gawk）解决这个问题。

### 1.1.2. FreeBSD
FreeBSD附带二进制包和源包：
#### 安装二进制包
```
$ pkg install erlang git gmake
```
在 FreeBSD 上，make命令是 BSD Make。 请改用 gmake。

### 1.1.3. OS X and macOS
虽然 Apple 分发他们自己的 GNU Make，但他们的版本非常陈旧，并且存在许多错误。 建议从Homebrew 或 MacPorts 安装更新版本：
#### Homebrew. 
```
$ brew install erlang git make
```
Homebrew 将 GNU Make 安装为 gmake。 make 命令是 Apple 提供的命令。
#### MacPorts. 
```
$ sudo port install erlang git gmake
```