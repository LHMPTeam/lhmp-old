project(sqlite)

set(SQLITE_SOURCE_FILES
	shell.c
	sqlite3.c
	)
set(SQLITE_HEADER_FILES
	sqlite3.h
	sqlite3ext.h
	SQLiteResultPool.h
	)


add_library(sqlite ${SQLITE_SOURCE_FILES} ${SQLITE_HEADER_FILES})
