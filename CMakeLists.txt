cmake_minimum_required(VERSION 3.25)
project(super_mario_lewis_glasgow)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)

include(FetchContent)
FetchContent_Declare(SFML
        GIT_REPOSITORY https://github.com/SFML/SFML.git
        GIT_TAG 2.6.x)
FetchContent_MakeAvailable(SFML)

add_executable(super_mario_lewis_glasgow
        main.cpp
        Player.cpp
        Player.h
        TileEditor.cpp
        TileEditor.h
        TileEntity.cpp
        TileEntity.h)

target_link_libraries(super_mario_lewis_glasgow PRIVATE sfml-graphics sfml-window sfml-system sfml-audio)