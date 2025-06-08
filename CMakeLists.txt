cmake_minimum_required(VERSION 3.20)
project(ScriptForge LANGUAGES CXX)

# Use C++20 or higher for best modern features
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Prefer using vcpkg toolchain (auto-detected by modern CMake/vcpkg integration)
# 推荐用 vcpkg 自动集成 (CMake 会自动找到 vcpkg 安装的库)

# Find ICU and uchardet using CMake's find_package
find_package(ICU REQUIRED COMPONENTS uc i18n data)     # Unicode support / Unicode 支持
find_package(uchardet REQUIRED)                        # Charset detection / 编码侦测

add_executable(scriptforge main.cpp)                   # Your source file(s) / 你的源文件

# Link dependencies (ICU and uchardet) / 链接依赖库
target_link_libraries(scriptforge
  PRIVATE
    ICU::uc ICU::i18n ICU::data
    uchardet
)

# Recommended: Set include directories for easier usage (if needed)
# 推荐：设置 include 目录（如需要）
# target_include_directories(scriptforge PRIVATE ${ICU_INCLUDE_DIRS} ${UCHARDET_INCLUDE_DIRS})

# Optional: Enable warnings / 选项：开启警告
target_compile_options(scriptforge PRIVATE
  $<$<CXX_COMPILER_ID:MSVC>:/W4>
  $<$<NOT:$<CXX_COMPILER_ID:MSVC>>:-Wall -Wextra -pedantic>
)

# --- Usage Example / 使用示例 ---
# 1. 在 main.cpp 里 include <unicode/unistr.h>, <uchardet/uchardet.h> 等
# 2. 用 vcpkg 安装依赖后直接构建即可