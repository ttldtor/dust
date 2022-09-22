cmake_minimum_required(VERSION 3.20)
project(dust)

set(CMAKE_CXX_STANDARD 20)

include(${CMAKE_BINARY_DIR}/conan_paths.cmake)

find_package(Boost)
find_package(fmt)
add_executable(dust src/main.cpp)

target_link_libraries(dust PRIVATE Boost::boost fmt::fmt-header-only)

if (NOT MSVC)
    find_package(Threads)
    target_link_libraries(dust PRIVATE Threads::Threads)
endif ()

if (WIN32)
    target_link_libraries(dust PRIVATE wsock32 ws2_32)
endif ()