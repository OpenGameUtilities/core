# Copyright (C) 2024 Open Game Utilities
#
# This file is part of OGU Core Library.
#
# OGU Core Library is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or (at
# your option) any later version.
#
# OGU Core Library is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with OGU Core Library.  If not, see <https://www.gnu.org/licenses/>.

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