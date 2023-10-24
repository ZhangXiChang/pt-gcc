#构建目标
get_filename_component(BUILD_TARGET_NAME ${CMAKE_CURRENT_SOURCE_DIR} NAME)
add_executable(${BUILD_TARGET_NAME})

#目标源代码
aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR}/src PRIVATE_SRC)
target_sources(${BUILD_TARGET_NAME} PRIVATE ${PRIVATE_SRC})
#目标包含目录
target_include_directories(${BUILD_TARGET_NAME} PRIVATE
)
#目标链接库
target_link_libraries(${BUILD_TARGET_NAME} PRIVATE
)
