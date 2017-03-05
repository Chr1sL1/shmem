project(host)

include_directories(../lib)
aux_source_directory(../lib SRC_DIR)
aux_source_directory(. SRC_DIR)

message(status, ${SRC_DIR})

add_compile_options(-g)
add_executable(host ${SRC_DIR})
target_link_libraries(host rt)

