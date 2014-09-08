cmake_minimum_required(VERSION 2.8.3)
project(pr2_pan_tilt)
find_package(catkin REQUIRED COMPONENTS geometry_msgs pr2_controllers_msgs topic_tools actionlib rospy tf)

catkin_package(
    DEPENDS geometry_msgs pr2_controllers_msgs topic_tools actionlib rospy tf
    CATKIN_DEPENDS # TODO
    INCLUDE_DIRS # TODO include
    LIBRARIES # TODO
)

install(FILES pantilt.jpg pan_tilt.launch pr2_pan_tilt.app pan_tilt.interface DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

install(PROGRAMS scripts/head_teleop.py DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
