cmake_minimum_required(VERSION 3.12)
project(net)

file(GLOB source_files
 		${PROJECT_SOURCE_DIR}/*.h
 		${PROJECT_SOURCE_DIR}/*.cpp)

add_library(net ${source_files})

target_include_directories(net PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(net
  Public src)