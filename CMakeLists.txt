cmake_minimum_required(VERSION 2.8)

project(pcd2vtk)

set(CMAKE_CXX_STANDARD 11)

find_package(PCL REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})

link_directories(${PCL_LIBRARY_DIRS})

add_definitions(${PCL_DEFINITIONS})

add_executable(pcd2vtk main.cpp)

target_link_libraries(pcd2vtk ${PCL_LIBRARIES})

install (TARGETS pcd2vtk RUNTIME DESTINATION bin)
