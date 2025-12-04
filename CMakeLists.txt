cmake_minimum_required(VERSION 3.10)

project(RTWeekend C CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CMAKE_C_STANDARD 23)
set(CMAKE_C_EXTENSIONS OFF)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(${PROJECT_NAME}
    src/main.cpp
    src/types.hpp
)

target_include_directories(${PROJECT_NAME}
PRIVATE
    src
)

target_compile_definitions(${PROJECT_NAME}
PRIVATE
    NOMINMAX
)

target_precompile_headers(${PROJECT_NAME}
PRIVATE
    src/pch.hpp
)
