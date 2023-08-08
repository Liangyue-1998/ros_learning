# ros_learning

## Configration
[source /opt/ros/humble/setup.bash](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html)https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html

## ROS2 command
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
      
## Compile command
Excute compile process after each fix
1. cd ~/dev_ws
2. colcon build
3. source install/local_setuo.sh

## create function package
cd ~/dev_ws/src
ros2 pkg create --build-type <build-type><package_name>
1. c++: ros2 pkg create --build-type ament_cmake learning_pkg_c
2. python: ros2 pkg create --build-type ament_python learning_pkg_python
   
## Node
1. Process
2. Independent executable document
3. Different languages
4. Distributed in the different desktop
5. Managed by the node name

## Node Programming: 
run command: ros2 run [package name] [class name]
#### OOP
1. Import package
   ```
   import rclpy
   from rclpy.node import Node
   ```
3. Initialize the interface:
   ```
   def main(args = None):
       rclpy.init(args = args)
   ```
4. Create node and initialize node:
   ```
   node = Node("node_helloworld")
   ```
5. Implement node function
6. Destroy and shutdown node
   ```
   node.destroy_node()
   rcply.shutdown()
   ```
#### OOP
 <img width="415" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/589d14e8-db60-4b30-8501-5e409785d6a3">

#### OOD
<img width="436" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/f4a4af4f-dd49-49b8-ac5b-279a8e05dc5f">

## Node setup
<img width="708" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/8dfc922f-2711-4853-9130-497097d2821e">




