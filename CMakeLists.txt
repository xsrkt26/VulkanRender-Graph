cmake_minimum_required(VERSION 3.29)
project(VulkanProject)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# --- Include 目录 ---
include_directories(
        ${CMAKE_SOURCE_DIR}/Dependency/GLFW/include
        ${CMAKE_SOURCE_DIR}/Dependency/Vulkan/Include
        ${CMAKE_SOURCE_DIR}/Dependency/glm
        ${CMAKE_SOURCE_DIR}/Dependency
)

# --- 链接库目录（MinGW下使用 .a） ---
link_directories(
        ${CMAKE_SOURCE_DIR}/Dependency/GLFW/lib-mingw-w64
        ${CMAKE_SOURCE_DIR}/Dependency/Vulkan/Lib
)

add_executable(VulkanProject main.cpp
        Dependency/stb_image.h
        VKStart.h
        VKBase.h
        GlfwGeneral.hpp)

# --- 链接静态库 ---
target_link_libraries(VulkanProject
        glfw3
        vulkan-1
)