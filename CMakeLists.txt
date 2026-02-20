cmake_minimum_required(VERSION 3.20)
project(OpenGLCube)

set(CMAKE_CXX_STANDARD 17)

find_package(GLEW REQUIRED)
find_package(glfw3 REQUIRED)
find_package(glm CONFIG REQUIRED)

add_executable(OpenGLCube main.cpp)

target_link_libraries(OpenGLCube
        PRIVATE
        GLEW::GLEW
        glfw
        GL
        glm::glm
)

