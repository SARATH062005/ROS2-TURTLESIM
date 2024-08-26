# ROS2-TURTLESIM

#Basic comments

ros2 pkg executables turtlesim
--turtlesim draw_square
--turtlesim mimic
--turtlesim turtle_teleop_key
--turtlesim turtlesim_node

ros2 run turtlesim turtlesim_node
--Warning: Ignoring XDG_SESSION_TYPE=wayland on Gnome. Use QT_QPA_PLATFORM=wayland to run on Wayland anyway.
--[INFO] [1724691874.312765932] [turtlesim]: Starting turtlesim with node name /turtlesim
--[INFO] [1724691874.333206587] [turtlesim]: Spawning turtle [turtle1] at x=[5.544445], y=[5.544445], theta=[0.000000]

ros2 run turtlesim turtle_teleop_key
--Reading from keyboard
---------------------------
Use arrow keys to move the turtle.
Use G|B|V|C|D|E|R|T keys to rotate to absolute orientations. 'F' to cancel a rotation.
'Q' to quit.

ros2 topic list

ros 2 topic info /turtle1/cmd_vel

ros2 topic echo /turtle1/cmd_vel

ros2 topic pub /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 1, y: 1, z:0}, angular: {x: 0, y: 0, z: 3.14}}"

#for revolution
ros2 topic pub --once /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 1, y: 1, z: 0}, angular: {x: 0, y: 0, z: 3.14}}"

