cmake_minimum_required(VERSION 2.8.3)

project(tu_nguyen)

find_package(catkin REQUIRED
urdf
controller_manager
joint_state_controller
robot_state_publisher
message_generation
rospy
)


catkin_package()

find_package(roslaunch)

foreach(dir config launch meshes urdf)
	install(DIRECTORY ${dir}/
		DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)
