CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

PROJECT(SM4)
set(CMAKE_C_COMPILER "clang")
include_directories(include)

aux_source_directory(src SM4_SRC)

add_library(SM4_LIB ${SM4_SRC})

add_executable(SM4 test/main.c)
set(CMAKE_CXX_STANDARD 11)
target_link_libraries(SM4 SM4_LIB)

SET(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -O2")