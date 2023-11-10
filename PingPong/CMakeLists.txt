# CMakeList.txt : CMake project for PingPong, include source and define
# project specific logic here.
#

project("PingPong")

find_package(Boost REQUIRED)

###############################
# Libs
###############################

###############################
# Headers
###############################
set(
	HEADERS
	"PingPong.h"
)

###############################
# Sources
###############################
set(
	SOURCES
	"PingPong.cpp"
)

# Add source to this project's executable.
add_executable (
	${PROJECT_NAME}
	${HEADERS} 
	${SOURCES}
	${LINK_LIBS}
)

#target_link_libraries(#
#	${PROJECT_NAME}
#	PRIVATE
#)

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET PingPong PROPERTY CXX_STANDARD 20)
endif()

# TODO: Add tests and install targets if needed.
