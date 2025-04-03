cmake_minimum_required(VERSION 4.0)

project(
  time_manager
  VERSION 0.1
  LANGUAGES CXX
)

set(CXX_STANDARD 26)

add_library(time_manager_lib
  ${CMAKE_CURRENT_SOURCE_DIR}/src/time_manager.cpp
)

target_include_directories(time_manager_lib PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}/include
)

add_executable( time_manager
  ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp
)

target_link_libraries(time_manager
  time_manager_lib
)
