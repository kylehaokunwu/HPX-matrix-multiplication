cmake_minimum_required(VERSION 3.18)
project(hpx_matrix_mul)

find_package(HPX REQUIRED)

add_executable(matrix_mul src/main.cpp)
target_link_libraries(matrix_mul HPX::hpx HPX::wrap_main)
