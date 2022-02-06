cmake_minimum_required(VERSION 3.20.0)

set(DTC_OVERLAY_FILE "${DTC_OVERLAY_FILE};project.overlay")
list(APPEND BOARD_ROOT ${CMAKE_CURRENT_SOURCE_DIR})
find_package(Zephyr)
project(PokiRobotSoft)

target_include_directories(app PRIVATE 
    lib
    lib/as5047p  lib/display  lib/ledinfo  lib/lidar  lib/motors  
    lib/obstacles  lib/pathfinding  lib/robot_utils  lib/servos  
    lib/speedgen  lib/strategy  lib/tirette  lib/wall_detector  lib/xoshiro128plusplus 
    inc
    inc/control  inc/flag  inc/match  inc/nav  inc/odometry  inc/thread_killer
)

file(GLOB_RECURSE APP_SOURCES 
    lib/*.c lib/*.cpp
    src/*.c src/*.cpp)      

target_sources(app PRIVATE ${APP_SOURCES})
