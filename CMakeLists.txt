cmake_minimum_required(VERSION 3.8)

set(APP_NAME "Template")

project(${APP_NAME})

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(Tests)
add_subdirectory(src)
add_subdirectory(lib)

include_directories(${templateLib_SOURCE_DIR})

aux_source_directory(. SRC)

add_executable(${APP_NAME} ${SRC})

target_link_libraries(${APP_NAME} templateLib)

#add_dependencies(${APP_NAME} RUN_UniTests)
