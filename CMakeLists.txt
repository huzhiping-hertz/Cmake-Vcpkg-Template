cmake_minimum_required (VERSION 3.10)
project("Drivers")

#set(VCPKG_FEATURE_FLAGS "1.0.0") 
#set(CMake_CXX_STANDARD 17)
#set(CMake_CXX_STANDARD_REQUARED ON)

#设置库信息

find_package(Poco CONFIG REQUIRED Net Util JSON Redis)
find_package(gflags CONFIG REQUIRED)
find_package(Catch2 CONFIG REQUIRED)
find_package(nlohmann_json CONFIG REQUIRED)
find_package(spdlog CONFIG REQUIRED)
find_package(httplib CONFIG REQUIRED)

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/src/Main)

#执行文件输出路径
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
#库文件输出路径
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

#项目源码
add_subdirectory(src/Main)
