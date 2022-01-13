cmake_minimum_required(VERSION 3.10)

project(LearningOpenGl VERSION 1.0)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_EXPORT_COMPILE_COMMANDS True)

add_executable(main src/main.cc src/glad.c)

find_package(glfw3 3.2 REQUIRED)
target_link_libraries(main PUBLIC glfw)

target_include_directories(main PUBLIC "include")
target_include_directories(main PRIVATE "/usr/local/include")
target_include_directories(main PRIVATE ${GLFW})
