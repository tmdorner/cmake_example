cmake_minimum_required(VERSION 3.0.0)
project(cmake_example VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

add_executable(cmake_example main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
install(TARGETS cmake_example DESTINATION /usr/bin)
