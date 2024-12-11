cmake_minimum_required(VERSION 3.5.0)
project(test VERSION 0.1.0 LANGUAGES C CXX)

add_executable(test src/main.cpp)

include(cmake/CPM.cmake)

add_subdirectory(libs/glfw)

target_link_libraries(${PROJECT_NAME} PRIVATE glfw )