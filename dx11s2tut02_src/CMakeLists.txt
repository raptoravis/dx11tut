cmake_minimum_required( VERSION 3.9.2 )

project(dx11tut)
 
  
 add_compile_definitions(UNICODE)

#Bring the headers, such as Student.h into the project
include_directories(source)

#Can manually add the sources using the set command as follows:
#set(SOURCES src/mainapp.cpp src/Student.cpp)

#However, the file(GLOB...) allows for wildcard additions:
file(GLOB SOURCES "source/*.cpp")

add_executable(dx11tut WIN32 ${SOURCES})