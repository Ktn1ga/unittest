cmake_minimum_required(VERSION 3.14)

set(_module_path "${CMAKE_CURRENT_SOURCE_DIR}/../../libs")
include(${_module_path}/tools/build_lib.cmake)

get_filename_component(project_dir ${CMAKE_CURRENT_SOURCE_DIR} NAME)
project("build_${project_dir}" LANGUAGES C)
project_share_lib(${_module_path} EXPORT_HEADERS "include/unity.h" "include/unity_internals.h")
