cmake_minimum_required(VERSION 3.0.0)
project(QLCode VERSION 0.1.0)

include(CTest)
enable_testing()

set(CMAKE_BUILD_TYPE Debug)
set(EXECUTABLE_OUTPUT_PATH ../output)

set(libs )
set(src )

set(src main.cpp)
set(libs )

add_executable(${PROJECT_NAME} ${src})
target_link_libraries(${PROJECT_NAME} ${libs})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
