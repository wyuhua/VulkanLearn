# CMakeList.txt: VKRender 的 CMake 项目，在此处包括源代码并定义
# 项目特定的逻辑。
#
cmake_minimum_required (VERSION 3.8)

project ("VKRender")

set(CMAKE_CXX_STANDARD 17)

#third party header and lib 
set(VULKAN_INCLUDE "C:/VulkanSDK/1.2.189.0/Include")
include_directories(${VULKAN_INCLUDE})

#set(SDL_INCLUDE "C:/VulkanSDK/1.2.189.0/Third-Party/Include/SDL2")
#include_directories(${SDL_INCLUDE})

set(GLFW_INCLUDE "C:/VulkanSDK/1.2.189.0/Third-Party/glfw-3.3.6.bin.WIN64/include")
include_directories(${GLFW_INCLUDE})

set(GLM_INCLUDE "C:/VulkanSDK/1.2.189.0/Third-Party/glm-0.9.9.8/glm")
include_directories(${GLM_INCLUDE})

#set(SDL_LIB "C:/VulkanSDK/1.2.189.0/Third-Party/Bin")
#link_directories(${SDL_LIB})

set(VULKAN_LIB "C:/VulkanSDK/1.2.189.0/Lib")
link_directories(${VULKAN_LIB})

set(GLFW_LIB "C:/VulkanSDK/1.2.189.0/Third-Party/glfw-3.3.6.bin.WIN64/lib-vc2019")
link_directories(${GLFW_LIB})

# 将源代码添加到此项目的可执行文件。
add_executable (VKRender "VKRender.cpp" "VKRender.h")
target_link_libraries(VKRender vulkan-1.lib glfw3.lib)

# TODO: 如有需要，请添加测试并安装目标。
