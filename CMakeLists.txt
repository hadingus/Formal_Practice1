cmake_minimum_required(VERSION 3.12.4)
project(Practice_formal_)

set(CMAKE_CXX_STANDARD 20)

include_directories(solution_src)
add_subdirectory(solution_src)
add_executable(Main main.cpp)
target_link_libraries(Main SolutionLib)