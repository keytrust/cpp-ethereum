add_library(webthree WebThree.cpp WebThree.h)

target_include_directories(webthree PRIVATE ..)
target_link_libraries(webthree whisper)

cotire(webthree)
