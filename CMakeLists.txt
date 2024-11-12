cmake_minimum_required(VERSION 3.5.0)
project(ASCII_Graphics VERSION 0.1.0 LANGUAGES C CXX)

# Compile commands for the IDE
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# CXX Standard
set(CMAKE_CXX_STANDARD 17) # CPP 17
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR})
set(BUILD_SHARED_LIBS OFF)

add_subdirectory(src)
add_subdirectory(external)


include(CTest)
enable_testing()

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
