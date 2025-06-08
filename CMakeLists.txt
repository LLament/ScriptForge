cmake_minimum_required(VERSION 3.16)
project(ScriptForge++ LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# 强制 MSVC 使用 UTF-8 编码 / Force MSVC to use UTF-8 source files
if (MSVC)
    add_compile_options("$<$<CXX_COMPILER_ID:MSVC>:/utf-8>")
endif()

# 头文件路径 / Include directories
include_directories(${CMAKE_SOURCE_DIR}/include)

# 源文件 / Source files
file(GLOB SRC_FILES src/*.cpp)

# 静态库目标 / Static library target
add_library(scriptforge STATIC ${SRC_FILES})

# 主程序入口 / Main program
add_executable(scriptforge_main src/main.cpp)
target_link_libraries(scriptforge_main scriptforge)

# 设置最终输出文件名为 ScriptForge++.exe
set_target_properties(scriptforge_main PROPERTIES
    OUTPUT_NAME "ScriptForge++"
)

# 测试入口 / Test main
add_executable(scriptforge_test tests/test_main.cpp)
target_link_libraries(scriptforge_test scriptforge)