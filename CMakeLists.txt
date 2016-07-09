cmake_minimum_required(VERSION 3.5)
project(openmp_sample)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES main.cpp)
if (APPLE)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fopenmp")
    set(CMAKE_CXX_COMPILER "/usr/local/bin/g++-6")
    set(CMAKE_C_COMPILER "/usr/local/bin/gcc-6")
endif ()


add_executable(openmp_sample ${SOURCE_FILES})