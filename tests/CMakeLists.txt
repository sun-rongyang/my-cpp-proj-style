macro(add_unittest TEST_NAME TEST_SRC CFLAGS INCLUDE_DIRS LINK_LIBS)
  add_executable(${TEST_NAME}
    ${TEST_SRC}
  )

  target_compile_options(${TEST_NAME}
    PRIVATE ${CFLAGS}
  )
  target_include_directories(${TEST_NAME}
    PRIVATE ${INCLUDE_DIRS}
  )
  target_link_libraries(${TEST_NAME}
    GTest::GTest GTest::Main
    "${LINK_LIBS}"
  )

  add_test(
    NAME ${TEST_NAME}
    COMMAND "${TEST_NAME}"
  )

  set_target_properties(${TEST_NAME} PROPERTIES FOLDER tests)
endmacro()


add_unittest(gtest_simple "gtest_simple.cc" "" "" "")