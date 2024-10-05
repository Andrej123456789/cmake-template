cmake_minimum_required(VERSION 3.16)

set(CMAKE_BUILD_TYPE Release)

project(cmake-test)

file(GLOB SRC CONFIGURE_DEPENDS "*.h" "*.c")

add_executable(${PROJECT_NAME} ${SRC})
target_link_libraries(${PROJECT_NAME} PRIVATE cmake-library)
target_include_directories(${PROJECT_NAME} PRIVATE "../include")
