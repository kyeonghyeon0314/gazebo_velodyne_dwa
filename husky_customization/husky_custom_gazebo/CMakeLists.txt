cmake_minimum_required(VERSION 2.8.3)
project(husky_custom_gazebo)

find_package(catkin)

catkin_package()
catkin_add_env_hooks(60.husky_custom_gazebo
  SHELLS sh DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/env-hooks)

install(
  DIRECTORY urdf launch worlds config models
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
