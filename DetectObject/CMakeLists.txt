# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.8)

# Using C++14 because we need a few components present in it
# Please Update Compiler On Target System to Latest VERSION
# Update Other Applications as well
set (CMAKE_CXX_STANDARD 14)

project ("DetectObject")

find_package(OPENCV REQUIRED)

INCLUDE_DIRECTORIES(PRIVATE ${OPENCV_INCLUDE_DIR})

# Add source to this project's executable.
add_executable (DetectObject "main.cxx"
							 "include/Shapes.hxx"
							 "include/Window.hxx"
							 "include/CircularObjectDetector.hxx" )

target_link_libraries( DetectObject PRIVATE ${OpenCV_LIBS} )
