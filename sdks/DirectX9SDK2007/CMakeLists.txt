project(d3dx)


if("${CMAKE_GENERATOR}" MATCHES "(Win64|IA64)")
    set(D3D_LIBS 
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/d3dx8.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/d3dx8d.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/d3dx8dt.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/d3dxd.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/d3dxof.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/ddraw.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/dinput.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/dinput8.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/dplayx.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/dsound.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/DxErr.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/DxErr8.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/dxgi.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/dxguid.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/dxtrans.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/X3DAudio.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x64/XInput.lib
)
else()
    set(D3D_LIBS
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/d3d8.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/d3dx8.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/d3dx8d.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/d3dx8dt.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/d3dxd.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/d3dxof.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/ddraw.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/dinput.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/dinput8.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/dplayx.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/dsetup.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/dsound.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/DxErr.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/DxErr8.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/dxgi.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/dxguid.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/dxtrans.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/X3DAudio.lib
        ${CMAKE_CURRENT_SOURCE_DIR}/Lib/x86/XInput.lib
)
endif()

add_library(d3dsdk INTERFACE)
target_link_libraries(d3dsdk INTERFACE ${D3D_LIBS})
#target_link_libraries(d3dsdk INTERFACE ${D3D8SDK_LIB_LIST})
target_include_directories(d3dsdk INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)
