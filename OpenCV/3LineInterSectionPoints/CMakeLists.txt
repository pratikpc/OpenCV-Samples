﻿# CMakeList.txt : CMake project for OpenCV VideoPlayer include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

set (CMAKE_CXX_STANDARD 17)

project(3LineInterSectionPoints)

find_package(OpenCV REQUIRED)
INCLUDE_DIRECTORIES(${OPENCV_INCLUDE_DIR})

# Add source to this project's executable.
add_executable (3LineInterSectionPoints "main.cxx" "include/Window.hxx" "include/Image.hxx" )

target_link_libraries( 3LineInterSectionPoints ${OpenCV_LIBS} )

# TODO: Add tests and install targets if needed.
