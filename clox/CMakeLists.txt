cmake_minimum_required(VERSION 3.10)
project(clox C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)

file(GLOB SOURCES CONFIGURE_DEPENDS src/*.c)

add_executable(clox ${SOURCES})

target_include_directories(clox PRIVATE include)

target_compile_options(clox PRIVATE -Wall -Wextra -Werror)
