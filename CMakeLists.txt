cmake_minimum_required(VERSION 3.0.0)
project(lab3-3-tututrr-patch-1 VERSION 0.1.0)

include(CTest)
enable_testing()

add_subdirectory(googletest)
include_directories(googletest/include) 
add_executable(tests Test_lab3sem3.cpp)
target_link_libraries(tests PRIVATE gtest)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
