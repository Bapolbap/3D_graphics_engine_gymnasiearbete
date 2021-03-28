cmake_minimum_required(VERSION "3.20.0")
project(3D_PROJECT)

add_library(
    glad
    glad.h
    khrplatform.h
)

add_library(
    glfw
    glfw3.h
    glfw3native.h
)

set_target_properties(glad PROPERTIES LINKER_LANGUAGE C)
set_target_properties(glfw PROPERTIES LINKER_LANGUAGE C)

add_executable(${PROJECT_NAME} test.cpp glad.c)

target_link_libraries(${PROJECT_NAME} glad glfw)

