#*********************************************************************
# Copyright (C) Suirless, 2018-2020. All rights reserved.
# simdjson micro library for CMake
# Apache-2 License
#****************************************************************/

cmake_minimum_required(VERSION 3.16)
project(simdjson C CXX)

set(CMAKE_INCLUDE_CURRENT_DIRS ON)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)
set(SIMDJSON_JUST_LIBRARY ON)

file(GLOB SIMDJSON_SRC
    ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/*.h
)

add_library(simdjson STATIC ${SIMDJSON_SRC})
target_include_directories(simdjson PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
