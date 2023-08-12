cmake_minimum_required (VERSION 3.8)

project ("VulkanTest")
set(CMAKE_CXX_STANDARD 17)

include_directories(
  "/usr/include/vulkan/" 
  "/usr/include/"
)

FIND_LIBRARY(VULKAN NAMES vulkan)
FIND_LIBRARY(GLFW NAMES glfw)
FIND_LIBRARY(X11 NAMES X11)
FIND_LIBRARY(DL NAMES dl)
FIND_LIBRARY(PTHREAD NAMES pthread)
FIND_LIBRARY(XRANDR NAMES Xrandr)
FIND_LIBRARY(XI NAMES Xi)

add_executable (
  VulkanTest
  main.cpp 
)

TARGET_LINK_LIBRARIES(
  VulkanTest
  ${VULKAN}
  ${GLFW}
)