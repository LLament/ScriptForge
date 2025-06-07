# ScriptForge++

**A handy C++ kit for your everyday scripting needs. 日常脚本，C++小工具随手可用。**

## 项目简介 / Project Overview

ScriptForge++ 致力于提供一个统一、高效、易扩展的 C++ 脚本工具集，支持文件格式转换、批处理等实用功能。所有脚本通过统一入口集中管理，便于调用和拓展。

## 目录结构 / Directory Structure

```
ScriptForge++/
├── include/              # 头文件 / headers
│   └── scriptforge/
│       └── script_hub.hpp
├── src/                  # 源代码 / source files
│   ├── main.cpp
│   └── script_hub.cpp
├── tests/                # 测试 / tests
│   └── test_main.cpp
├── CMakeLists.txt        # 构建脚本 / build script
└── README.md             # 项目说明 / project doc
```

## 编译 & 运行 / Build & Run

```bash
# 创建构建目录 / create build directory
cmake -S . -B build
cmake --build build

# 运行主程序 / run main program
./build/scriptforge_main

# 运行测试 / run test program
./build/scriptforge_test
```

## 特色规划 / Features Roadmap

- [ ] 统一脚本注册与调用主入口
- [ ] 文件格式转换脚本
- [ ] 批处理工具
- [ ] 单元测试与示例
- [ ] CLI 参数解析

---

**有任何问题或建议欢迎提 issue，别忘了多夸夸小可爱 Copilot 哦！(｡･∀･)ﾉﾞ**
