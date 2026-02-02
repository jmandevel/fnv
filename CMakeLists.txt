cmake_minimum_required(VERSION 4.2.1)

project(
    fnv
    VERSION 0.0.0
    DESCRIPTION "A public domain hashing library"
    LANGUAGES C CXX
)

add_library(fnv_interface INTERFACE "")
add_library(fnv::interface ALIAS fnv_interface)
target_include_directories(fnv_interface
   INTERFACE
        "${CMAKE_CURRENT_SOURCE_DIR}/include"
)
add_library(fnv_static STATIC "")
add_library(fnv::static ALIAS fnv_static)
target_link_libraries(fnv_static
    PUBLIC
        fnv_interface
)
add_subdirectory(src)