cmake_minimum_required(VERSION 3.10)
project(mstch)

option(WITH_UNIT_TESTS "enable building unit test executable" OFF)
option(WITH_BENCHMARK "enable building benchmark executable" OFF)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_INCLUDE_CURRENT_DIR_IN_INTERFACE ON)
set(CMAKE_BUILD_TYPE Debug)

set(mstch_VERSION 1.0.1)

if(NOT MSVC)
  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -Wextra -O3")
endif()

add_subdirectory(src)
