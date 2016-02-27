cmake_minimum_required(VERSION 2.8.3)
project(thermaleye_msgs)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

add_message_files(
  FILES
  Mapping.msg
)

generate_messages(
    DEPENDENCIES
)

catkin_package(
    DEPENDS 
    CATKIN_DEPENDS std_msgs message_runtime# TODO
    INCLUDE_DIRS  ${catkin_INCLUDE_DIRS}
    LIBRARIES # TODO
)

#install(DIRECTORY include/${PROJECT_NAME}/
#  DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
#  FILES_MATCHING PATTERN "*.h")
