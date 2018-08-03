project(md5)

set(MD5_SOURCE_FILES
	md5.cpp
	)

set(MD5_HEADER_FILES
	md5.h
	)

add_library(md5 ${MD5_SOURCE_FILES} ${MD5_HEADER_FILES})
