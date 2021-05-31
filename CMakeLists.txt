cmake_minimum_required(VERSION 3.12)
project("CppWithMklAndGtest")

find_package(GTest REQUIRED)
message($ENV{MKLROOT})