cmake_minimum_required (VERSION 2.6)

project (vm)

SET(CMAKE_CXX_FLAGS  "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -Werror")

find_package(Boost REQUIRED COMPONENTS system filesystem)

add_executable(vm
  vm.cpp
  parser.cpp
  code.cpp
)

target_link_libraries(vm ${Boost_LIBRARIES})
