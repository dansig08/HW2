cmake_minimum_required(VERSION 3.2)
project(HW2)
set(CMAKE_CXX_STANDARD 20)

set(mySRC ${CMAKE_SOURCE_DIR}/src) 
set(myInclude ${CMAKE_SOURCE_DIR}/include)

set(SDL2_LIBRARIES "${CMAKE_SOURCE_DIR}/lib/SDL2d.lib;${CMAKE_SOURCE_DIR}/lib/SDL2maind.lib")

include_directories(${CMAKE_SOURCE_DIR} ${CMAKE_SOURCE_DIR}/lib/SDL)

add_executable(${CMAKE_PROJECT_NAME} #main.cpp Plane.h Plane.cpp ATC.h
target_link_libraries(${CMAKE_PROJECT_NAME}

ATC.cpp ${mySRC}/HW2_Visualizer.h ${mySRC}/HW2_Visualizer.cpp)

"${CMAKE_SOURCE_DIR}/lib/SDL2d.lib;${CMAKE_SOURCE_DIR}/lib/SDL2maind.lib")

set_target_properties( ${CMAKE_PROJECT_NAME} PROPERTIES

RUNTIME_OUTPUT_DIRECTORY_DEBUG "${CMAKE_BINARY_DIR}/bin")

# Copy the dynamic library to the same folder as the executable file.

add_custom_command(TARGET ${CMAKE_PROJECT_NAME} POST_BUILD #

Adds a post-build event to MyTest

COMMAND ${CMAKE_COMMAND} -E copy_if_different # which executes

"cmake - E copy_if_different..."

"${CMAKE_SOURCE_DIR}/lib/SDL2d.dll" # <--this is in-

file

"${CMAKE_SOURCE_DIR}/map.bmp" # <--this

is also in-file

$<TARGET_FILE_DIR:${CMAKE_PROJECT_NAME}>) # <--this is out-

file path

