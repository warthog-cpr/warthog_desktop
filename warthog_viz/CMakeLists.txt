cmake_minimum_required(VERSION 3.0.2)
project(warthog_viz)

find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()

roslaunch_add_file_check(launch/view_diagnostics.launch)
roslaunch_add_file_check(launch/view_model.launch)
roslaunch_add_file_check(launch/view_robot.launch)

install(DIRECTORY launch rqt rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
