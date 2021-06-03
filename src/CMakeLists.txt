add_executable(using_mkl using_mkl.cc)
target_include_directories(using_mkl PRIVATE /usr/include/mkl)