add_library(
    glad
    glad/glad.h
    glad/khrplatform.h
)

add_library(
    glfw
    GLFW/glfw3.h
    GLFW/glfw3native.h
)

set_target_properties(glad PROPERTIES LINKER_LANGUAGE C)
set_target_properties(glfw PROPERTIES LINKER_LANGUAGE C)

target_include_directories(glad PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/glad)
target_include_directories(glfw PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/GLFW)