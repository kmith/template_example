cmake_minimum_required(VERSION 3.4 FATAL_ERROR)

project(laplace_equation VERSION 1.0 LANGUAGES C Fortran)

find_package(OpenCMISSLibs 1.3.0 REQUIRED COMPONENTS Iron CONFIG)

add_subdirectory(src/fortran)
