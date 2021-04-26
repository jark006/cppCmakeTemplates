cmake_minimum_required(VERSION 2.8)

project(CPPTEST)

IF (NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE "Release" CACHE STRING
        "Choose the type of build, options are: Debug Release RelWithDebInfo MinSizeRel." FORCE)
ENDIF()

include_directories(include)

aux_source_directory(src SRC_LIST)

add_executable(${PROJECT_NAME} ${SRC_LIST})

#math lib
target_link_libraries(${PROJECT_NAME} m)


