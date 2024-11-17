cmake_minimum_required(VERSION 3.5)
project(multithreaded_bubble_sort)

find_package(TBB REQUIRED)
include_directories(${TBB_INCLUDE_DIR})

add_executable(multithreaded_bubble_sort main.cpp)
target_link_libraries(multithreaded_bubble_sort ${TBB_LIBRARIES} PUBLIC TBB::tbb)

