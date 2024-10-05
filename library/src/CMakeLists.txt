cmake_minimum_required(VERSION 3.16)

set(CMAKE_BUILD_TYPE Release)

project(cmake-library)

file(GLOB SRC CONFIGURE_DEPENDS "*.h" "*.c")

add_library(${PROJECT_NAME} STATIC ${SRC})
target_link_libraries(${PROJECT_NAME})
target_include_directories(${PROJECT_NAME} PRIVATE "../include")

install(TARGETS ${PROJECT_NAME} DESTINATION lib)
install(FILES "../include/cmake_library.h" DESTINATION include)
