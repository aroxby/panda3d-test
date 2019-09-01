cmake_minimum_required(VERSION 2.6)

set(PROJECT_NAME panda3d-test)
project(${PROJECT_NAME})

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_SOURCE_DIR}/cmake)
find_package(Panda3d REQUIRED)
set(PANDA3D_LIBRARIES ${PANDA3D_INCLUDE_DIR}/../lib/libpanda.lib)

include_directories(${PANDA3D_INCLUDE_DIR})

file(GLOB SRCS *.cpp)

add_executable(${PROJECT_NAME} ${SRCS})

target_link_libraries(${PROJECT_NAME} ${PANDA3D_LIBRARIES})
