configure_file (test_config.hh.in
  ${PROJECT_BINARY_DIR}/include/test_config.hh
)

add_subdirectory(gtest_vendor)
add_subdirectory(helpers)
add_subdirectory(integration)
add_subdirectory(performance)
add_subdirectory(plugins)
add_subdirectory(regression)
