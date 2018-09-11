add_library(detours INTERFACE)
target_link_libraries(detours INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/lib/detours.lib)
target_include_directories(detours INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)
