#---------------------------------------------------------------------------------------------------
# CMake Build Configuration for the Ray Tracing Weekend Series
#
# See README.md for guidance.
#---------------------------------------------------------------------------------------------------

cmake_minimum_required ( VERSION 3.1.0...4.0.0 )

project ( Raytracer LANGUAGES CXX )

# Set to C++11
set ( CMAKE_CXX_STANDARD          11 )
set ( CMAKE_CXX_STANDARD_REQUIRED ON )
set ( CMAKE_CXX_EXTENSIONS        OFF )

# Add sources
set ( SOURCE_RAYTRACER 
    src/main.cc
    src/vec3.h
    src/color.h
    src/ray.h
    src/hittable.h
    src/sphere.h
 "src/hittable_list.h" "src/util.h" "src/interval.h" "src/camera.h" "src/material.h")

include_directories(src)

# Add executable
add_executable ( raytracer ${SOURCE_RAYTRACER})