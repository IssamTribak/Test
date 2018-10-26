cmake_minimum_required(VERSION 3.12)
project(lisp)

file(GLOB source_files
 		${PROJECT_SOURCE_DIR}/*.h
 		${PROJECT_SOURCE_DIR}/*.cpp)

add_library(lisp ${source_files})

target_include_directories(lisp PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(lisp
  Public src)