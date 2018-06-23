cmake_minimum_required(VERSION 3.1)

set(CMAKE_C_COMPILER "D:/LLVM/bin/clang-cl.exe")
set(CMAKE_CXX_COMPILER "D:/LLVM/bin/clang-cl.exe")
set(CMAKE_FIND_ROOT_PATH "D:/LLVM/bin/")

project(GameEngineFromZero)
include_directories("${PROJECT_SOURCE_DIR}/Framework/Common")
include_directories("${PROJECT_SOURCE_DIR}/Framework/Interface")
add_subdirectory(Framework)
add_subdirectory(Empty)
