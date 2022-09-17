cmake_minimum_required (VERSION 3.10)

set(CMake_CXX_STANDARD 17)
set(CMake_CXX_STANDARD_REQUARED ON)

#设置库信息

find_package(Poco CONFIG REQUIRED Net XML Zip Data)
find_package(Crow CONFIG REQUIRED)
find_package(ZLIB REQUIRED)

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/src/Main)

#执行文件输出路径
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
#库文件输出路径
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

#项目源码
add_subdirectory(src/Main)
