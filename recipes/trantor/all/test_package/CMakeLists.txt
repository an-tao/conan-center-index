cmake_minimum_required(VERSION 3.4)
project(test_package)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

find_package(Trantor REQUIRED CONFIG)

add_executable(${PROJECT_NAME} test_package.cpp)
target_link_libraries(${PROJECT_NAME} PUBLIC Trantor::Trantor)
set_property(TARGET ${PROJECT_NAME} PROPERTY CXX_STANDARD 14)
