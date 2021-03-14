cmake_minimum_required(VERSION 3.17)

project(static_library)

add_library(message 
	SHARED
  	src/message.hpp
  	src/message.cpp
)

add_executable(hello-world src/hello_world.cpp)

target_link_libraries(hello-world message)