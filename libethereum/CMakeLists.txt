file(GLOB SRC_LIST "*.cpp")
file(GLOB HEADERS "*.h")

add_library(ethereum ${SRC_LIST} ${HEADERS})

target_include_directories(ethereum PRIVATE ..)
target_include_directories(ethereum PRIVATE ../utils)
target_link_libraries(ethereum evm p2p JsonCpp)

cotire(ethereum)
