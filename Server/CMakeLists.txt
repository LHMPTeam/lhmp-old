cmake_minimum_required(VERSION 3.0)

project(lhmp-server)

set(LHMP_SERVER_SOURCES
	CBanSystem.cpp
	CConfig.cpp
	CConsole.cpp
	CCore.cpp
	CDoorPool.cpp
	CEntity.cpp
	CFileTransfer.cpp
	CGameMode.cpp
	CLog.cpp
	CMasterServer.cpp
	CNetworkManager.cpp
	CPickup.cpp
	CPickupPool.cpp
	CPlayer.cpp
	CPlayerPool.cpp
	CQueryServer.cpp
	CScript.cpp
	CScripts.cpp
	CTCP.cpp
	CTickManager.cpp
	CTimer.cpp
	CTimerPool.cpp
	CVehicle.cpp
	CVehiclePool.cpp
	Main.cpp
	sq_funcdef.cpp
	sq_functions.cpp
	sq_utils.cpp
	squirrelheads.cpp
	)

add_executable(server ${LHMP_SERVER_SOURCES})
target_link_libraries(server RakNet squirrel sqlite udplib sqstdlib md5 ${CMAKE_THREAD_LIBS_INIT} ${CMAKE_DL_LIBS})
#target_include_directories(server PRIVATE
#	${CMAKE_CURRENT_SOURCE_DIR}/../sdks/RakNet
#	${CMAKE_CURRENT_SOURCE_DIR}/../sdks/SQUIRREL3/include
#	)
