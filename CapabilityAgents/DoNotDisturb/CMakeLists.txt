cmake_minimum_required(VERSION 3.0)
project(DoNotDisturbCA VERSION ${PROJECT_VERSION} LANGUAGES CXX)

include(../../build/BuildDefaults.cmake)

add_subdirectory("src")
add_subdirectory("test")
