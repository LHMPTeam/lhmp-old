project(UDPwrapper)

set(UDP_SOURCE_FILES
	clhmpquery.cpp
	UDPWrapper.cpp
	)

set(UDP_HEADER_FILES
	clhmpquery.h
	UDPWrapper.h
	)

add_library(udplib ${UDP_SOURCE_FILES} ${UDP_HEADER_FILES})

if(LHMP_BUILD_DEMO)
	add_executable(querydemo Source.cpp)
	target_link_libraries(querydemo udplib)

	add_executable(udpdemo UDPSource.cpp)
	target_link_libraries(udpdemo udplib)
endif()
