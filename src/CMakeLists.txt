cmake_minimum_required(VERSION 3.16)
# appveyor does not build modorganizer in its standard location, so use
# DEPENDENCIES_DIR to find cmake_common
if(DEFINED DEPENDENCIES_DIR)
	include(${DEPENDENCIES_DIR}/modorganizer_super/cmake_common/src.cmake)
else()
	include(../cmake_common/src.cmake)
endif()
add_definitions(-DMODORGANIZER_ARCHIVE_BUILDING)
