cmake_minimum_required(VERSION 3.22)
project(DllInjector)

set(CMAKE_CXX_STANDARD 14)

set(${CMAKE_CXX_FLAGS} "${CMAKE_CXX_FLAGS} -static-libgcc -static-libstdc++ -static -mwindows")


add_executable(DllInjector main.cpp include/GLFW/glfw3.h include/GLFW/glfw3native.h include/GLFW/glfw3native.h)

target_link_libraries(DllInjector ${CMAKE_SOURCE_DIR}/lib/glfw3.lib)