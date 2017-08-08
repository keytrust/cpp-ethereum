aux_source_directory(. SRC_LIST)

file(GLOB HEADERS "*.h")

add_library(ethcore ${SRC_LIST} ${HEADERS})

target_include_directories(ethcore PRIVATE .. ../utils)
target_include_directories(ethcore PRIVATE )
target_link_libraries(ethcore devcrypto devcore)

cotire(ethcore)
