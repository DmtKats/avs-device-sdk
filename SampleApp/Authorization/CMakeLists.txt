cmake_minimum_required(VERSION 3.1 FATAL_ERROR)
project(Authorization VERSION ${PROJECT_VERSION} LANGUAGES CXX)

include(../../build/BuildDefaults.cmake)

add_subdirectory("CBLAuthDelegate")
