include(AddCatch2)

add_executable(unittest ./src/test_calc.cpp)
target_link_libraries(unittest PRIVATE calculator Catch2::Catch2WithMain)

include(CTest)
include(Catch)
catch_discover_tests(unittest)