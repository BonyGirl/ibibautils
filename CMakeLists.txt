cmake_minimum_required(VERSION 2.8)
project(libibautils)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -fPIC") 
set(CMAKE_C_FLAGS "$CMAKE_C_FLAGS -fPIC")
set(LIBIBAUTILS "ibautils")
set(CMAKE_BUILD_TYPE Release)
add_library(cpp-lib SHARED ${CPP_FILES})

add_definitions(-Wall -std=c++0x -fPIC)

# RE2
SET(RE2_DIR ${PROJECT_SOURCE_DIR})
FIND_PACKAGE(RE2 REQUIRED)

INCLUDE_DIRECTORIES(${RE2_INCLUDE_DIR})

ADD_SUBDIRECTORY("src")
