project(petrel-root)
cmake_minimum_required(VERSION 2.8)

set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake)

add_subdirectory(src)

option(DISABLE_TESTS "Do not build unit tests.")

if(NOT DISABLE_TESTS STREQUAL "on")
  enable_testing()
  add_subdirectory(test)
endif(NOT DISABLE_TESTS STREQUAL "on")
