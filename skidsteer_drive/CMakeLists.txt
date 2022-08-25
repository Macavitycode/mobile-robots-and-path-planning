cmake_minimum_required(VERSION 2.8.3)
project(skidsteer_drive)

find_package(catkin REQUIRED COMPONENTS
    xacro
)

catkin_package()

include_directories(
    ${catkin_INCLUDE_DIRS}
)
