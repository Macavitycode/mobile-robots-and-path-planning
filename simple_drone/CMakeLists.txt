cmake_minimum_required(VERSION 2.8.3)
project(simple_drone)

find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
)
include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
