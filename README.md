# MotomanMH-ROS2
ROS2 port of motoman_mh_support from motoman_experimental, demonstrating bugs with the VSCode URDF Preview

Ported from https://github.com/ros-industrial/motoman_experimental.

# Building
Use colcon build from the root of the workspace.
This package depends on xacro.

# Replicating the mirroring bug in VSCode
(Windows, ROS v0.9.5 Pre-Release)
1) Source your ROS2 Humble install
2) Build the package with colcon build
3) Source the package with the install\local_setup.ps1
4) Run code to launch VSCode with 
5) Open the folder in VSCode.
6) Open urdf\mh180_120.xacro in VSCode.
7) Ctrl-Shift-P -> ROS: Preview URDF
8) View the incorrect display of URDF.
Many links are mirrored and rotated around such that the robot arm is no longer even connected!

All models are mirrored over their YZ planes. The origins of each model are in the correct position, but each model is mirrored.

# Screenshot:
Screenshots are attached to show the bug and proper appearance of the robot.

VSCode's incorrect display: VScode_Mirrored.png

Correct display of the same robot through RoboDK (This doesn't use URDF, but is the way the robot should appear): RoboDK_MH180_120.png

Correct display of the URDF using urdf-viz: urdf-viz_Correct.png
 
