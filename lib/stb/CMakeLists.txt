cmake_minimum_required(VERSION 3.22)
project(stb)

add_library(stb STATIC src/stb_image.cpp)
target_include_directories(stb PRIVATE include)