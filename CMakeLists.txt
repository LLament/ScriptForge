cmake_minimum_required(VERSION 3.16)
project(ScriptForge++ LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# 头文件路径 / Include directories
include_directories(${CMAKE_SOURCE_DIR}/include)

# 源文件 / Source files
file(GLOB SRC_FILES src/*.cpp)

add_library(scriptforge STATIC ${SRC_FILES})

# 测试可执行文件 / Example/Test executable
add_executable(scriptforge_test tests/test_main.cpp)
target_link_libraries(scriptforge_test scriptforge)