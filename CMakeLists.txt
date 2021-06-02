cmake_minimum_required(VERSION 3.12)
project("CppWithMklAndGtest")

find_package(GTest REQUIRED)

if(DEFINED ENV{MKLROOT})
    message("MKLROOT found" ENV{MKLROOT})
else()
    message("MKLROOT not found")
endif(DEFINED ENV{MKLROOT})

add_subdirectory(src)