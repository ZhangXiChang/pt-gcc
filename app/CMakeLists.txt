#构建目标
get_filename_component(BUILD_TARGET_NAME ${CMAKE_CURRENT_SOURCE_DIR} NAME)
add_executable(${BUILD_TARGET_NAME})

#目标源代码
aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR}/src PRIVATE_SRC)
target_sources(${BUILD_TARGET_NAME} PRIVATE ${PRIVATE_SRC})
