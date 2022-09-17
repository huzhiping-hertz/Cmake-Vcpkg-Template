cmake_minimum_required (VERSION 3.10)

set(CMake_CXX_STANDARD 17)
set(CMake_CXX_STANDARD_REQUARED ON)
#set (VCPKG_FEATURE_FLAGS "versions")

#设置库信息

find_package(Poco CONFIG REQUIRED Net XML Zip Data)
find_package(Crow CONFIG REQUIRED)
find_package(ZLIB REQUIRED)

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/src/Main)

#链接库搜索路径
#这个用于Debug版本
#LINK_DIRECTORIES(C:/work/vcpkg/installed/x64-windows/debug/lib)
#这个用于Release版本
LINK_DIRECTORIES(${VCPKG_DIR}/lib)

#执行文件输出路径
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
#库文件输出路径
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

#项目源码
add_subdirectory(src/Main)
