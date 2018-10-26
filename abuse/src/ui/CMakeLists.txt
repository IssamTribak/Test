cmake_minimum_required(VERSION 3.12)
project(ui)



file(GLOB source_files
 		${PROJECT_SOURCE_DIR}/*.h
 		${PROJECT_SOURCE_DIR}/*.cpp)

add_library(ui ${source_files})



target_include_directories(ui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(ui
  Public src)
