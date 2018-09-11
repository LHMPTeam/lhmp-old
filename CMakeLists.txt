cmake_minimum_required(VERSION 3.0)
project(lhmp CXX)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)


option(LHMP_BUILD_MASTERLIST "Build masterlist - only for LHMP maintainers" OFF)
if(WIN32)
    option(LHMP_BUILD_LOADER "Build Loader for injecting client" ON)
    option(LHMP_BUILD_CLIENT "Build client DLL" ON)
endif()

set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/modules)
message("Module path: ${CMAKE_MODULE_PATH}")

find_package(Threads REQUIRED)


add_subdirectory(sdks)
add_subdirectory(Server)

if(LHMP_BUILD_MASTERLIST)
    add_subdirectory(MasterList)
endif()

if(WIN32)
    if(LHMP_BUILD_LOADER)
        add_subdirectory(Loader)
    endif()
    if(LHMP_BUILD_CLIENT)
        add_subdirectory(Client)
    endif()
endif()
