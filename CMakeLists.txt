cmake_minimum_required(VERSION 2.8.3)
project(rtt_control_state_msgs)

find_package(catkin REQUIRED COMPONENTS 
  rtt_roscomm
)

ros_generate_rtt_typekit(control_state_msgs)
ros_generate_rtt_service_proxies(control_state_msgs)

orocos_generate_package(
  DEPENDS control_state_msgs
  DEPENDS_TARGETS rtt_roscomm rtt_actionlib_msgs
)
