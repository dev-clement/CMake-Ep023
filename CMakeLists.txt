#[==[
    . Introducing testing
    . Using the catch2 as an example
#]==]

cmake_minimum_required(VERSION 3.20)

project(Dependencies)

enable_testing()

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(calculator)

add_executable(rooster main.cpp)
target_link_libraries(rooster PRIVATE calculator)

add_subdirectory(test)