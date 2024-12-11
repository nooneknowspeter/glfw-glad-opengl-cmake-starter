cmake_minimum_required(VERSION 3.5.0)
project(test VERSION 0.1.0 LANGUAGES C CXX)

cmake_policy(SET CMP0072 NEW)

find_package(OpenGL REQUIRED)

add_executable(test src/main.cpp)

include(cmake/CPM.cmake)

add_subdirectory(libs/glfw)
add_subdirectory(libs/glad)

target_link_libraries(${PROJECT_NAME} PRIVATE glfw glad OpenGL::GL)