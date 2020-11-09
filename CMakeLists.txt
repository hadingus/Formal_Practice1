cmake_minimum_required(VERSION 3.12.4)
project(Practice_formal_)

set(CMAKE_CXX_STANDARD 20)
find_package(GTest REQUIRED)
include_directories(${GTEST_INCLUDE_DIR} solution_src)
add_subdirectory(solution_src)

add_executable(CTests main_test.cpp gtests/tests.cpp)
target_link_libraries(CTests Threads::Threads ${GTEST_LIBRARIES} ${GMOCK_BOTH_LIBRARIES} SolutionLib)

add_executable(Main main.cpp)
target_link_libraries(Main SolutionLib)