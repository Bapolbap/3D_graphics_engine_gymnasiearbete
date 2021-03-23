add_executable(${PROJECT_NAME} test.cpp glad.c)

target_link_libraries(${PROJECT_NAME} glad glfw)
