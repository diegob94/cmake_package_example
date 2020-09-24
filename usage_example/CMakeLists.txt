cmake_minimum_required(VERSION 3.17)

PROJECT(example)
set(CMAKE_NO_SYSTEM_FROM_IMPORTED on)

add_executable(${PROJECT_NAME} src/example.cpp)

find_package(mylib CONFIG REQUIRED)
target_link_libraries(${PROJECT_NAME} mylib)

