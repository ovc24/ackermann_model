cmake_minimum_required(VERSION 2.8.3)

project(ackermann_model)

find_package(catkin REQUIRED)

catkin_package()

catkin_install_python(PROGRAMS scripts/ackermann_controller
                      DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

install(DIRECTORY config launch meshes urdf scripts
		DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

