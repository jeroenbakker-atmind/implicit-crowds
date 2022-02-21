cmake_minimum_required(VERSION 3.6)
set(CMAKE_CXX_STANDARD 14)

project(implicit_crowds)

option(WITH_CALLISTO "Show simulation using Callisto" Off)

if (WITH_CALLISTO)
    add_compile_options(-DWITH_CALLISTO)
endif()

add_subdirectory(library)


add_executable(implicit library/src/Main.cpp)
target_include_directories(implicit PUBLIC library/include external)

target_link_libraries(implicit implicit_lib)
