cmake_minimum_required(VERSION 2.8.12)
project(fanuc_j519_msgs)

find_package(catkin REQUIRED
  COMPONENTS
    message_generation
    std_msgs
)

add_message_files(
  DIRECTORY
    msg
  FILES
    Command.msg
    IoTypes.msg
    RobotState.msg
    ThresholdRequest.msg
    ThresholdResponse.msg
    ThresholdTypes.msg
)

generate_messages(
  DEPENDENCIES
    std_msgs
)

catkin_package(
  CATKIN_DEPENDS
    message_runtime
    std_msgs
)
