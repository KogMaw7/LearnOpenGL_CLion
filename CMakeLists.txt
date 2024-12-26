cmake_minimum_required(VERSION 3.28)
project(LearnOpenGL_CLion)

set(CMAKE_CXX_STANDARD 17)

add_subdirectory(lib)

include_directories(${GLFW3_INCLUDE_DIR} ${GLAD_INCLUDE_DIR})

add_executable(LearnOpenGL_CLion main.cpp)
target_link_libraries(LearnOpenGL_CLion glfw glad)