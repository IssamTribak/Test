cmake_minimum_required(VERSION 3.12)
project(imlib)

file(GLOB source_files
 		${PROJECT_SOURCE_DIR}/*.h
 		${PROJECT_SOURCE_DIR}/*.cpp)

add_library(imlib ${source_files})

target_include_directories(imlib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(imlib
  Public src)

