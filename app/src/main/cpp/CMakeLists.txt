cmake_minimum_required(VERSION 3.22.1)

project("platinmods")

set(CMAKE_CXX_STANDARD 20)
set(dobby_home ${CMAKE_CURRENT_SOURCE_DIR}/Dobby/dobby.a)

add_library(
        ${CMAKE_PROJECT_NAME}
        SHARED
        Main.cpp
)

target_link_libraries(
        ${CMAKE_PROJECT_NAME}
        android
        log
        ${dobby_home}
)