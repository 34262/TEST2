cmake_minimum_required(VERSION 3.0)
project(test)
set(CMAKE_CXX_STANDARD 11)
#set(HOME /home/yanghao/TEST2)

# 设置默认构建类型为Debug（如果没有指定）
if (NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Debug)
endif()
set(HOME /home/yanghao/vscodedemo/test_makefike_json/TEST2)
file(GLOB SRC_LIST ${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp)
include_directories(${PROJECT_SOURCE_DIR}/include)
set(EXECUTABLE_OUTPUT_PATH ${HOME}/bin)
add_executable(app ${SRC_LIST})

message(STATUS "Source files: ${HOME}")
message(STATUS "Source files: ${CMAKE_CURRENT_SOURCE_DIR}")
message(STATUS "Source files: ${PROJECT_SOURCE_DIR}")