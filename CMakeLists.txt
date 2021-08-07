cmake_minimum_required(VERSION 3.12)
project("MyCppProjStyle"
    DESCRIPTION "My C++ project style includes code formatting, testings, documenting, IC/CD actions, etc" 
    LANGUAGES CXX
)

# Set MKL related PATHs
set(MKL_INCLUDE_DIR "/usr/include/mkl" CACHE PATH "MKL header file mkl.h include directory")
set(MKL_LINK_DIR "/usr/lib/x86_64-linux-gnu" CACHE PATH "MKL library link directory")
message(${MKL_INCLUDE_DIR})


add_subdirectory(src bin)


## Build GTest based unittests
# Find GoogleTest
find_package(GTest REQUIRED)
enable_testing()
add_subdirectory(tests tests)
