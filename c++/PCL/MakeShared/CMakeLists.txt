cmake_minimum_required(VERSION 2.6 FATAL_ERROR)
project(MakeShared)
find_package(PCL 1.0 REQUIRED COMPONENTS io)
include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})
add_executable(MakeShared MakeShared.cpp)
target_link_libraries(MakeShared ${PCL_COMMON_LIBRARIES} ${PCL_IO_LIBRARIES})
