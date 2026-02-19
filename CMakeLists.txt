cmake_minimum_required(VERSION 3.20)
project(untitled2 CXX)

set(CMAKE_CXX_STANDARD 17)

# 1. Find the library packages on your Linux system
find_package(PkgConfig REQUIRED)
pkg_check_modules(GLFW REQUIRED glfw3)
pkg_check_modules(GLEW REQUIRED glew)

# 2. Tell CMake about your source file
add_executable(untitled2 main.cpp)

# 3. LINK the libraries (This fixes the 'undefined reference' errors)
# We need to link: GLEW, GLFW, and the system OpenGL (GL)
target_link_libraries(untitled2 GLEW glfw GL)