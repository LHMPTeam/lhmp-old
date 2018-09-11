project(d3dfont)

set(D3DFONT_LIST 
    d3dfont.cpp
    d3dfont.h
    d3dutil.cpp
    d3dutil.h
    dxutil.cpp
    dxutil.h
)

add_library(d3dfont ${D3DFONT_LIST})
target_link_libraries(d3dfont PRIVATE d3dsdk)

