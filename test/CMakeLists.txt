cmake_minimum_required(VERSION 3.2)
project(${PROJECT_NAME}_tests)

add_subdirectory(lib/googletest)

include_directories(${HEADERS_DIR})
include_directories(lib/googletest/googletest/include)

set(SOURCE_FILES main.cpp src/divider_tests.cpp)

add_executable(${PROJECT_NAME}_tests ${SOURCE_FILES})
target_link_libraries(${PROJECT_NAME}_tests ${PROJECT_NAME}_lib gtest)
install(TARGETS ${PROJECT_NAME}_tests DESTINATION bin)

