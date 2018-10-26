cmake_minimum_required(VERSION 3.12)
project(ab)


file(GLOB source_files
 		${PROJECT_SOURCE_DIR}/*.h
 		${PROJECT_SOURCE_DIR}/*.cpp)

add_subdirectory(imlib)
add_subdirectory(lisp)
add_subdirectory(lol)
add_subdirectory(net)
add_subdirectory(sdlport)
add_subdirectory(ui)



 		
add_library(src ${source_files})




add_executable(abuse ${source_files}) 	

add_executable(abuse-tool ${source_files}) 	



target_link_libraries(abuse
	Public imlib
	Public lisp
	Public lol
	Public net
	Public sdlport
	Public ui
)

target_link_libraries(abuse-tool
	Public imlib
	Public lisp
	Public lol
	Public net
	Public sdlport
	Public ui
)


target_link_libraries(src
	Public imlib
	Public lisp
	Public lol
	Public net
	Public sdlport
	Public ui
	Public tool
)



target_include_directories(src PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})