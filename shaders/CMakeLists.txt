cmake_minimum_required(VERSION 3.20)

project(shaders)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

add_executable(app
    src/main.cpp
    ../external/glad/src/glad.c
)

target_include_directories(app PRIVATE 
    ../external/glad/include)

target_link_libraries(app
    glfw
    OpenGL::GL
)
