cmake_minimum_required(VERSION 4.0.2)
project(novagalaxynatsu)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/$<CONFIGURATION>")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/$<CONFIGURATION>")

add_subdirectory(vendored/SDL EXCLUDE_FROM_ALL)

add_executable(main ../src/main.cpp)

target_link_libraries(main PRIVATE SDL3::SDL3)