project(masterlist)

set(MASTERLIST_SOURCE_LIST
	CServers.cpp
	Main.cpp
	CNetwork.cpp
	)

set(MASTERLIST_HEADER_LIST
	CServers.h
	CNetwork.h
	CCore.h
	)

add_executable(masterlist ${MASTERLIST_SOURCE_LIST} ${MASTERLIST_HEADER_LIST})
target_link_libraries(masterlist udplib ${CMAKE_THREAD_LIBS_INIT})
