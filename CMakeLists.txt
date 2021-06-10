cmake_minimum_required(VERSION 3.12)
project("CppWithMklAndGtest"
    DESCRIPTION "A demo to show how to test a Intel MKL and GoogleTest used C++ project using Github Action"
    LANGUAGES CXX
)

# Set MKL related PATHs
set(MKL_INCLUDE_DIR /usr/include/mkl)
set(MKL_LINK_DIR /usr/lib/x86_64-linux-gnu)


add_subdirectory(src bin)


## Build GTest based unittests
# Find GoogleTest
find_package(GTest REQUIRED)
enable_testing()
add_subdirectory(tests tests)