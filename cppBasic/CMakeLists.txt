cmake_minimum_required(VERSION 2.8)

project(CPPTEST)

include_directories(include)

aux_source_directory(src SRC_LIST)

add_executable(${PROJECT_NAME} ${SRC_LIST})

#math lib
target_link_libraries(${PROJECT_NAME} m)


