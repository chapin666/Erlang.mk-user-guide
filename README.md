# Erlang.mk 用户指南

### 作者：

Loïc Hoguin

<essen@ninenines.eu>

### 译者:

chapin

v56b87@gmail.com

***

## 目录

### 一、 安装
  1. [Uinx 安装](./chapter1/on_uinx.md)
  2. [Windows 安装](./chapter1/on_windows.md)

### 二、入门
  1. [为你的项目创建文件夹](./chapter2/creating_a_folder_for_your_project.md)
  2. [下载 Erlang.mk](./chapter2/downloading_erlang.mk.md)
  3. [OTP application 入门](./chapter2/getting_started_with_OTP_applications.md)
  4. [OTP libraries 入门](./chapter2/getting_started_with_OTP_libraries.md)
  5. [OTP releases 入门](./chapter2/getting_started_with_OTP_releases.md)
  6. [从 scratch 开始](./chapter2/getting_started_from_scratch.md)
  7. [使用 spaces 代替 tabs](./chapter2/using_spaces_instead_of_tabs.md)
  8. [使用 templates](./chapter2/using_templates.md)
  9. [在 git 中隐藏 Erlang.mk](./chapter2/hiding_erlang.mk_from_git.md)
  10. [获取帮助](./chapter2/getting_help.md)

### 三、总结
  1. [构建你的项目](./chapter3/building_your_project.md)
  2. [探索包索引](./chapter3/exploring_the_package_index.md)
  3. [文档生成](./chapter3/generating_documentation.md)
  4. [运行测试](./chapter3/running_tests.md)
  5. [了解更多](./chapter3/need_more.md)

### 四、更新 Erlang.mk
  1. [初始化 bootstrap](./chapter4/initial_bootstrap.md)
  2. [更新](./chapter4/updating.md)
  3. [自定义构建](./chapter4/customizing_the_build.md)

### 五、限制
  1. [Erlang必须可用](./chapter5/erlang_must_be_available.md)
  2. [路径中的空格](./chapter5/spaces_in_path.md)
  3. [依赖关系跟踪和修改时间](./chapter5/dependency_tracking_and_modification_times.md)

## Ⅰ、Code
### 六、构建
  1. [怎么构建]()
  2. [构建什么]()
  3. [应用资源文件]()
  4. [自动应用程序资源文件值]()
  5. [文件格式化]()
  6. [编译选项]()
  7. [冷、热构建]()
  8. [依赖跟踪]()
  9. [生成 Erlang 代码]()
  10. [Cleaning]()

### 七、包和依赖
  1. [搜索包]()
  2. [添加依赖到项目]()
  3. [如何获取和构建 deps]()
  4. [提取和列出依赖项]()
  5. [忽略不需要的依赖项]()
  6. [依赖目录]()
  7. [多应用程序一个存储库]()
  8. [没有应用程序的根目录存储库]()
  9. [自动补丁]()
  10. [跳过 deps]()

### 八、NIF和端口驱动
  1. [C 源代码位置和 Erlang 环境]()
  2. [使用自定义 Makefile]()
  3. [直接使用 Erlang.mk]()
  4. [将编译和链接器标志传播到子 Makefile]()

### 九、发布
  1. [安装]()
  2. [配置]()
  3. [生成发布]()
  4. [运行发布]()
  5. [更新发布]()
  6. [获得 Relx semver 值]()

### 十、自解压版本
  1. [生成自解压存档]()
  2. [运行发布]()

### 十一、Escripts
  1. [先行条件]()
  2. [生成 escript]()
  3. [配置]()
  4. [额外的文件]()
  5. [优化大小]()

### 十二、OTP版本管理
  1. [Erlang 版本]()
  2. [OTP 版本固定]()
  3. [持续集成]()
  4. [配置 Kerl]()

### 十三、与其他构建工具的兼容性
  1. [Rebar 为 Erlang.mk 依赖项]()
  2. [Erlang.mk 为 Rebar 依赖项]()

## Ⅱ、文档
### 十四、AsciiDoc文档
  1. [要求]()
  2. [编写AsciiDoc文档]()
  3. [配置]()
  4. [使用]()

### 十五、EDoc注释
  1. [编写 EDoc 注释]()
  2. [配置]()
  3. [使用]()

### 十六、Sphinx 文档
  1. [编写 Sphinx 文档]()
  2. [基本安装]()
  3. [Erlang.mk 配置]()
  4. [生成 man 页面]()

## Ⅲ、Tests
### 十七、 Erlang shell
  1. [配置]()
  2. [使用]()

### 十八、EUnit
  1. [编写 tests]()
  2. [配置]()
  3. [使用]()

### 十九、常见 Test
  1. [编写 tests]()
  2. [配置]()
  3. [使用]()

### 二十、[Triq]()

### 二十一、[代码覆盖率]()

### 二十二、持续集成
  1. [配置要测试的 Erlang/OTP 版本]()
  2. [跨所有配置版本运行测试]()
  3. [扩展 CI 目标]()

### 二十三、Dialyzer
  1. [工作原理]()
  2. [配置]()
  3. [运行]()

### 二十四、[Xref]()

## Ⅳ、三方 plugins
### 二十五、扩展插件
  1. [从依赖项加载所有插件]()
  2. [从依赖项加载一个插件]()
  3. [编写外部插件]()
  4. [早期插件]()
  5. [加载应用程序本地的插件]()

### 二十六、插件列表
  1. [efene.mk]()
  2. [elixir.mk]()
  3. [elvis.mk]()
  4. [geas]()
  5. [hexer.mk]()
  6. [hexpm.mk]()
  7. [jorel]()
  8. [lfe.mk]()
  9. [mix.mk]()
  10. [reload.mk]()
  11. [rust.mk]()

## Ⅴ、关于 Erlang.mk
### 二十七、Why Erlang.mk
  1. [Erlang.mk 很快]()
  2. [Erlang.mk 为您提供 Unix 的全部功能]()
  3. [Erlang.mk 是一个文本文件]()
  4. [Erlang.mk 可以管理 Erlang 本身]()
  5. [Erlang.mk 可以做的不仅仅是 Erlang]()
  6. [Erlang.mk 在 Make 和 Automake 项目中很好地集成]()

### 二十八、简史
  1. [在Erlang.mk之前]()
  2. [项目的生命周期]()

### 二十九、Contributing
  1. [优先级]()
  2. [Bugs]()
  3. [代码]()
  4. [包]()
  5. [文档]()
  6. [功能请求]()



 

