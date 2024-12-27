add_subdirectory(glfw-3.4)
set(GLFW3_INCLUDE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/glfw-3.4/include" PARENT_SCOPE)
set(GLFW3_LIBRARY "${CMAKE_CURRENT_SOURCE_DIR}/glfw-3.4/src/libglfw3.a" PARENT_SCOPE)

add_subdirectory(glad)
set(GLAD_INCLUDE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/glad/include" PARENT_SCOPE)
set(GLAD_LIBRARY "${CMAKE_CURRENT_SOURCE_DIR}/glad/src/glad.o" PARENT_SCOPE)

add_subdirectory(stb)
set(STB_INCLUDE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/stb/include" PARENT_SCOPE)
set(STB_LIBRARY "${CMAKE_CURRENT_SOURCE_DIR}/stb/src/stb_image.o" PARENT_SCOPE)