cmake_minimum_required(VERSION 3.28)
project(ogu_core_library)
add_subdirectory(ogu)

# Formatter
add_custom_target(
  format
  COMMAND clang-format
  -style="file:${CMAKE_SOURCE_DIR}/.clang-format"
  -i
  "${CMAKE_SOURCE_DIR}/ogu/src/*.cpp"
  "${CMAKE_SOURCE_DIR}/ogu/inc/*.cppx"
)