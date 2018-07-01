cmake_minimum_required(VERSION 3.1)

aux_source_directory(. DIR_ROOT_SRCS)

MESSAGE(STATUS "platform: ${CMAKE_HOST_SYSTEM_NAME}")

IF (CMAKE_HOST_SYSTEM_NAME MATCHES "Linux")  
    set(CMAKE_C_COMPILER "/usr/bin/clang-6.0")
    set(CMAKE_CXX_COMPILER "/usr/bin/clang++-6.0")
ELSEIF (CMAKE_HOST_SYSTEM_NAME MATCHES "Windows")  
    set(CMAKE_C_COMPILER "D:/LLVM/bin/clang-cl.exe")
    set(CMAKE_CXX_COMPILER "D:/LLVM/bin/clang-cl.exe")
    set(CMAKE_FIND_ROOT_PATH "D:/LLVM/bin/")  
ELSE ()  
    MESSAGE(STATUS "other platform: ${CMAKE_HOST_SYSTEM_NAME}")
ENDIF (CMAKE_HOST_SYSTEM_NAME MATCHES "Linux") 

project(GameEngineFromZero)

include_directories("${PROJECT_SOURCE_DIR}/Framework/Common")
include_directories("${PROJECT_SOURCE_DIR}/Framework/Interface")

add_subdirectory(Framework)
add_subdirectory(Empty)
add_subdirectory(Platform)