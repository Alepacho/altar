cmake_minimum_required(VERSION 3.27)

set(PROJECT_NAME "altar")
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_SOURCE_DIR}/")
set(CMAKE_CXX_STANDARD 20)

project(${PROJECT_NAME} CXX)
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/3rdparty/fmt/)
find_package(fmt)

add_executable(${PROJECT_NAME}
    ${CMAKE_CURRENT_LIST_DIR}/src/main.cpp
)

target_link_libraries(${PROJECT_NAME}
    PRIVATE
    fmt::fmt-header-only
)
