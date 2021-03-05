cmake_minimum_required(VERSION 3.17)
project(driver_cruise)

set(CMAKE_CXX_STANDARD 14)

add_library(driver_cruise SHARED driver_cruise.cpp driver_cruise.h driver_cruise.def osspec.h tgf.h)
set_target_properties(driver_cruise PROPERTIES COMPILE_FLAGS "/Gd" ) #_cdecl
set_target_properties(driver_cruise PROPERTIES COMPILE_FLAGS "/Oi" ) #inline