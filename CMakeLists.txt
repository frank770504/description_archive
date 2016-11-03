cmake_minimum_required(VERSION 2.4.6)
project(agv2_description)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  roscpp
  roslib
  std_msgs
  urdf
  hector_gazebo_plugins
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS roscpp roslib std_msgs urdf
  DEPENDS 
)

#~ add_executable(motion_test src/motion_test.cpp)

#~ target_link_libraries(motion_test
  #~ ${catkin_LIBRARIES}
#~ )

install(DIRECTORY urdf
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

