cmake_minimum_required(VERSION 3.8)

set(LIB_NAME templateLib)

project(${LIB_NAME})

aux_source_directory(. SRC)

add_library(${LIB_NAME} ${SRC})