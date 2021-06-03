add_executable(using_mkl using_mkl.cc)
target_include_directories(using_mkl PRIVATE /usr/include/mkl)
target_link_directories(using_mkl PRIVATE /usr/lib/x86_64-linux-gnu)
target_link_libraries(using_mkl PRIVATE mkl_rt)