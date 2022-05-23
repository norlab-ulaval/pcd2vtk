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

# uninstall target
if(NOT TARGET uninstall)
  configure_file(
    "${CMAKE_CURRENT_SOURCE_DIR}/cmake_uninstall.cmake.in"
    "${CMAKE_CURRENT_BINARY_DIR}/cmake_uninstall.cmake"
    IMMEDIATE @ONLY)

  add_custom_target(uninstall
    COMMAND ${CMAKE_COMMAND} -P ${CMAKE_CURRENT_BINARY_DIR}/cmake_uninstall.cmake)
endif()

