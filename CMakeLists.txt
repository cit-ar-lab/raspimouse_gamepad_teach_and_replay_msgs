cmake_minimum_required(VERSION 2.8.3)
project(raspimouse_gamepad_teach_and_replay_msgs)

find_package(catkin REQUIRED COMPONENTS
    sensor_msgs
    raspimouse_ros_2
    geometry_msgs
    actionlib_msgs
    message_generation
)

add_message_files(FILES
    PFInformation.msg
    RaspiMouseEvent.msg
    LaserScanEvent.msg
    RaspiMouseIMULaserScanEvent.msg
)

generate_messages(DEPENDENCIES
    std_msgs
    sensor_msgs
    geometry_msgs
    raspimouse_ros_2
)

catkin_package(
    CATKIN_DEPENDS
    roscpp
    message_runtime
    raspimouse_ros_2
)