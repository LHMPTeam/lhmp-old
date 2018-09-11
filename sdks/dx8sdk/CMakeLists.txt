project(d3d8)

set(D3D8SDK_LIB_LIST
    lib/amstrmid.lib
    lib/d3d8.lib
    lib/d3dx.lib
    lib/d3dx8.lib
    lib/d3dx8d.lib
    lib/d3dx8dt.lib
    lib/d3dxd.lib
    lib/d3dxof.lib
    lib/ddraw.lib
    lib/dinput.lib
    lib/dinput8.lib
    lib/dmoguids.lib
    lib/dplayx.lib
    lib/dsetup.lib
    lib/dsound.lib
    lib/DxErr8.lib
    lib/dxguid.lib
    lib/dxtrans.lib
    lib/ksproxy.lib
    lib/ksuser.lib
    lib/msdmo.lib
    lib/quartz.lib
    lib/strmiids.lib
)

add_library(d3d8sdk INTERFACE)
target_link_libraries(d3d8sdk INTERFACE ${D3D8SDK_LIB_LIST})
target_include_directories(d3d8sdk INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)
