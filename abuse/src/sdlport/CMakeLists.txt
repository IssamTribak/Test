cmake_minimum_required(VERSION 3.12)
project(sdlport)

file(GLOB source_files
 		${PROJECT_SOURCE_DIR}/*.h
 		${PROJECT_SOURCE_DIR}/*.cpp)

add_library(sdlport ${source_files})

target_include_directories(sdlport PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

find_package(SDL REQUIRED)
include_directories(${SDL_INCLUDE_DIR})

target_link_libraries(sdlport
  Public src)