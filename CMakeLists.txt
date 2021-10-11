cmake_minimum_required(VERSION 3.16)
project(endomersion)

find_package(catkin REQUIRED COMPONENTS
        esvr2_ros
        franka_pivot_control_ros
        pivot_control_messages_ros
        #mediassist3_simulation
        roscpp)

catkin_package()
include_directories(${catkin_INCLUDE_DIRS})

catkin_install_python(PROGRAMS scripts/ControlUserStudy.py
        DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
        )