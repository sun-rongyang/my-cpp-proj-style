add_executable(using_mkl using_mkl.cc)
target_include_directories(using_mkl PRIVATE ${MKL_INCLUDE_DIR})
target_link_directories(using_mkl PRIVATE ${MKL_LINK_DIR})
target_link_libraries(using_mkl PRIVATE mkl_rt)