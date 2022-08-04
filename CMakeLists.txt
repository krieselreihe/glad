cmake_minimum_required(VERSION 3.22)

project(
  Glad
  DESCRIPTION "Multi-Language GL/GLES/EGL/GLX/WGL Loader-Generator based on the official specs."
  LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(LIBRARY "glad")

project(${LIBRARY})

add_library(${LIBRARY} include/glad/glad.h src/glad.c include/KHR/khrplatform.h)
target_include_directories(${LIBRARY} PUBLIC include/)
