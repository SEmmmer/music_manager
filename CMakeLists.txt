cmake_minimum_required(VERSION 3.15)
project(music_manager)

set(CMAKE_CXX_STANDARD 14)

include_directories(/usr/local/Cellar/taglib/1.11.1/include)
link_directories(/usr/local/Cellar/taglib/1.11.1/bin)

add_executable(music_manager main.cpp)
add_executable(test test.cpp)


target_link_libraries(music_manager ssl crypto)

#add_library(base64 STATIC base64.c)
#add_library(WjCryptLib_Rc4 STATIC WjCryptLib_Rc4.c)

#target_link_libraries(music base64)
#target_link_libraries(test base64)
#target_link_libraries(test WjCryptLib_Rc4)