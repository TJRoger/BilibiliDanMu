cmake_minimum_required(VERSION 3.15)
project(BilibiliDanMu)
set(CMAKE_CXX_STANDARD 17)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17")

include_directories(/usr/local/include)
link_directories(/usr/local/lib)
link_libraries(libPocoNet.dylib)

add_executable(BilibiliDanMu main.cpp)
target_link_libraries(BilibiliDanMu PRIVATE libPocoNet.dylib libz.a libjsoncpp.dylib)
