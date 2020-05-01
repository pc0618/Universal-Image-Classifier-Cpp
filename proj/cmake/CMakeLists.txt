cmake_minimum_required( VERSION 2.8 FATAL_ERROR )
set( CMAKE_VERBOSE_MAKEFILE ON )

project( ImageFileBasic )

get_filename_component( CINDER_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../../../.." ABSOLUTE )
get_filename_component( APP_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../../" ABSOLUTE )

include( "${CINDER_PATH}/proj/cmake/modules/cinderMakeApp.cmake" )


find_package(Torch REQUIRED)
find_package(OpenCV REQUIRED)
include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable(network ${APP_PATH}/src/network.cpp)
target_link_libraries(network "${TORCH_LIBRARIES}" "${OpenCV_LIBS}")
set_property(TARGET network PROPERTY CXX_STANDARD 14)

ci_make_app(
	SOURCES     ${APP_PATH}/src/ImageFileBasicApp.cpp
	CINDER_PATH ${CINDER_PATH}
)

