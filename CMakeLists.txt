cmake_minimum_required(VERSION 2.8.3)
project(turtlebot_random_walker)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  roscpp
  rospy
  sensor_msgs
  std_msgs
  move_base_msgs
)

catkin_package()

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

add_executable(walker src/main.cpp)
target_link_libraries(walker ${catkin_LIBRARIES})