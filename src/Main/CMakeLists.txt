set(APP_NAME "Main")
file(GLOB src_files "*.cpp")
add_executable(${APP_NAME} ${src_files})
target_link_libraries(${APP_NAME} PRIVATE  nlohmann_json httplib::httplib)