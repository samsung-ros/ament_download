cmake_minimum_required(VERSION 3.5)

set(catkin_EXTRAS_DIR ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

project(colcon_download)

find_package(ament_cmake REQUIRED)

set(AMENT_BUILD_CONFIGURATION_KEYWORD_SEPARATOR ":")

include("cmake/colcon_download.cmake")

# install cmake files for catkin
install(DIRECTORY cmake
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
  USE_SOURCE_PERMISSIONS
)

ament_export_dependencies(ament_cmake)
ament_package()
