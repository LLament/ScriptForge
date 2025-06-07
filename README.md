# ScriptForge++

> **Craft your scripts, forge your workflow!**  
> 用现代C++锻造多功能高效脚本工具集！

---

## 🛠️ 项目简介 | Project Overview

**ScriptForge++** is a modern C++ toolkit designed to empower developers with a collection of high-efficiency scripting utilities, all forged with elegance, extensibility, and cross-platform compatibility in mind.  
**ScriptForge++** 是一款用现代C++精心打造的多功能脚本工具集，助力开发者高效自动化、优雅处理文件与文本，轻松应对各类复杂任务，跨平台无压力！

---

## ✨ 特性亮点 | Features

- **Modern C++ (C++20/23)**  
  Leveraging modern language features for safety, clarity, and performance.  
  利用现代C++特性，安全、清晰、高性能。

- **All-in-One Scripting Toolbox**  
  File operations, text processing, automation, batch tools… all in one place!  
  文件操作、文本处理、自动化、批量工具，一站式集成！

- **Easy to Extend**  
  Clean modular design for painless customization.  
  模块化设计，轻松扩展和自定义。

- **Cross-Platform**  
  Windows, Linux, macOS — forge scripts anywhere!  
  全平台支持，随处锻造你的脚本！

- **Bilingual Documentation**  
  All comments and docs are English + 中文，国际范儿满满～  
  全部注释和文档中英双语，助力全球开发者！

---

## 🚀 快速上手 | Quick Start

```cpp
#include <scriptforge/file_utils.hpp>
#include <scriptforge/text_utils.hpp>
#include <iostream>

// Batch rename files in a directory
// 批量重命名目录下的文件
int main() {
    using namespace scriptforge;

    // Rename all ".log" files to "archived_*.log"
    // 将所有 .log 文件重命名为 archived_*.log
    batch_rename("*.log", "archived_*.log");

    // Count how many times "error" appears in a file
    // 统计"error"在文件中的出现次数
    auto count = count_occurrences_in_file("server.log", "error");
    std::cout << "Number of errors: " << count << std::endl; // 输出错误次数

    return 0;
}
```

---

## 🧰 目录结构 | Project Structure

```text
scriptforge++/
├── include/
│   └── scriptforge/
│       ├── file_utils.hpp    # File utilities | 文件工具
│       ├── text_utils.hpp    # Text utilities | 文本工具
│       └── ...               # More modules   | 更多模块
├── src/
├── tests/
└── README.md
```

---

## 🤝 贡献指南 | Contributing

Pull requests and issues are welcome!  
欢迎提交PR与建议，一起打造最强C++脚本工坊！

- Please keep code clean, modern, and well-commented (English + 中文).
- 请保持代码整洁、现代，并使用中英双语注释。

---

## 📄 许可证 | License

MIT

---

**ScriptForge++** — Where scripts are crafted, not cobbled!  
**ScriptForge++** —— 让脚本开发成为匠心艺术！
