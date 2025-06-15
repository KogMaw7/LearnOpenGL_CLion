cmake_minimum_required(VERSION 3.28)
project(LearnOpenGL_CLion)

set(CMAKE_CXX_STANDARD 17)

add_subdirectory(lib)

include_directories(${GLFW3_INCLUDE_DIR} ${GLAD_INCLUDE_DIR} ${STB_INCLUDE_DIR})

add_executable(LearnOpenGL_CLion main.cpp)
target_link_libraries(LearnOpenGL_CLion glu32.lib gdi32.lib)
target_link_libraries(LearnOpenGL_CLion glfw glad stb)

# 对于Windows平台，需要额外链接opengl32
if(WIN32)
    target_link_libraries(LearnOpenGL_CLion opengl32)
endif()

# 遍历Practice目录下所有的 .cpp 文件
file (GLOB files Practice/*/*cpp)
foreach (file ${files})
    string(REGEX REPLACE ".+/(.+)\\..*" "\\1" exe ${file})
    add_executable (${exe} ${file})
    target_link_libraries(${exe} glu32.lib gdi32.lib)
    target_link_libraries(${exe} glfw glad)
    if(WIN32)
        target_link_libraries(${exe} opengl32)
    endif()
    message (\ \ \ \ --\ src/${exe}.cpp\ will\ be\ compiled\ to\ bin/${exe})
endforeach ()