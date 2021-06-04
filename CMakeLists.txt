cmake_minimum_required(VERSION 3.12)
project("CppWithMklAndGtest"
    DESCRIPTION "A demo to show how to test a Intel MKL and GoogleTest used C++ project using Github Action"
    LANGUAGES CXX
)

# Set MKL related PATHs
set(MKL_INCLUDE_DIR /usr/include/mkl)
set(MKL_LINK_DIR /usr/lib/x86_64-linux-gnu)
# Find GoogleTest
find_package(GTest REQUIRED)


add_subdirectory(src)