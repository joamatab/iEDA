cmake_minimum_required(VERSION 3.11)
SET (CMAKE_CXX_STANDARD 20)

aux_source_directory(./ SRC)

add_library(time STATIC ${SRC})

target_link_libraries(time absl::time)

target_include_directories(time 
    PUBLIC 
        ${CMAKE_CURRENT_SOURCE_DIR}
)