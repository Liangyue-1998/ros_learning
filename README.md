# ros_learning

### Configration
[source /opt/ros/humble/setup.bash](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html)https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html

### ROS2 command
turtlesim simulation
1. ros2 run turtlesim turtlesim_node
2. ros2 run demo_nodes_cpp talker
3. ros info (subscriber/publisher/service)
   ros2 node info /turtlesim
4. ros2 topic
   ros2 topic list
   ros2 topic echo /turtle1/pose
   ros2 topic pub
5. save data
   1. ros2 bag
   2. ros2 bag record /turtle1/cmd_vel
      pause: ctrl + C
      path: current path of terminal
   3. data review
      ros2 bag play [filename]/
      
