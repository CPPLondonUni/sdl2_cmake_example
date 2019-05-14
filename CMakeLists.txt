
cmake_minimum_required(VERSION 3.1)

project(cmake_sdl2_example CXX)

add_executable(my_game src/main.cpp)

# Add necessary CMake info here to find SDL2

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${cmake_sdl2_example_SOURCE_DIR}/cmake")

find_package(SDL2 REQUIRED)

target_include_directories(my_game PUBLIC ${SDL2_INCLUDE_DIR})

target_link_libraries(my_game ${SDL2_LIBRARY})
