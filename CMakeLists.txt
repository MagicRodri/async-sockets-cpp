cmake_minimum_required(VERSION 3.0.0)
project(async-sockets)

set(asyncSockets_INCLUDE_DIRS ${CMAKE_CURRENT_SOURCE_DIR}/include)

include_directories(asyncSockets_INCLUDE_DIRS)

add_library(async-sockets SHARED src/udpserver.cpp src/tcpserver.cpp src/udpsocket.cpp src/tcpsocket.cpp)

target_include_directories(async-sockets PUBLIC include)

INSTALL(
  DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/
  DESTINATION include)