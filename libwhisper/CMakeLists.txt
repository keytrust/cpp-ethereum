aux_source_directory(. SRC_LIST)

file(GLOB HEADERS "*.h")

add_library(whisper ${SRC_LIST} ${HEADERS})

target_include_directories(whisper PRIVATE ..)
target_include_directories(whisper PRIVATE ../utils)
target_link_libraries(whisper p2p)

cotire(whisper)