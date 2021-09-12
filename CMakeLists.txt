cmake_minimum_required(VERSION 3.14)
project(HelloWorld)
set(EXE_NAME HelloWorld)

set(input01 "helloworld.py")

foreach (file IN LISTS input01)
    configure_file(${file} ${file} COPYONLY)
endforeach ()

set(CMAKE_CXX_STANDARD 17)

add_executable(${EXE_NAME} main.cpp)
