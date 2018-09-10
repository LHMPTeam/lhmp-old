cmake_minimum_required(VERSION 3.0)

project(lhmp CXX)

set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/modules)
message("Module path: ${CMAKE_MODULE_PATH}")

find_package(Threads REQUIRED)


add_subdirectory(sdks)
add_subdirectory(Server)
add_subdirectory(MasterList)
add_subdirectory(Loader)
