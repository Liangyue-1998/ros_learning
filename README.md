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
2. rosdepc install -i --from-path src --rosdistro humble -y
3. colcon build --symlink-install
4. source install/local_setup.sh

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

## Message: Node topic communication
1. Publisher/subscripter models
2. Asynchronization
3. Message structure: .msg file

#### Publisher
<img width="913" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/46fd5ecb-4044-4408-a413-b8981f4f97ad">


#### Subscriber
<img width="641" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/b207173a-23b0-4841-8e40-9f0625ee7416">

#### usb camera in ros
- sudo apt install ros-humble-camera
- Publisher node: ros2 run usb_cam usb_cam_node_exe
- Subscriber node: ros2 run [package name] [class name]

#### Topic command
- ros2 topic list
- ros2 topic info
- ros2 topic bw
- ros2 topic info /image_raw
- ros2 topic bw /image_raw
- ros2 topic echo /image_raw 
- rqt_graph 

## Node service and client (request & response)
1. Service and client
2. Synchronization
3. Unique service and mutiple client
4. Data structure: .srv file
<img width="563" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/72a8cdc5-e63a-44eb-b1d1-583b5c7e7249">

#### Client 
1. Initilize the interface
2. Create node and initilize the node
3. Create client object
4. Send request
5. Wait for the response from service
6. Destroy and shutoff the node
<img width="661" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/57ddf052-22c9-4132-b038-758174c1827f">
 
#### Service
1. Initilize the interface
2. Create node and initilize the node
3. Create service object
4. callback function
5. send response to the client
6. Destroy and shutoff the node
<img width="895" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/72778f10-2fe8-44d6-a35d-4f7e6a5f13ab">

#### Example
<img width="874" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/03b8908c-6d7e-4d39-95e6-1b09ab609ca1">

#### Service command
- ros2 servicee list

## Communication interface structure
<img width="825" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/464c5a17-a62c-4c25-b147-ade3e9f355d7">
<img width="825" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/922ad531-8a16-4567-8c00-125bfc5d073a">
from [packge] import [interface name]

#### command
<img width="890" alt="image" src="https://github.com/Liangyue-1998/ros_learning/assets/61789633/beb9d543-667a-4f52-933d-a5501268922f">
- ros2 interface list
- ros2 interface show [interface name]


## DDS (Data Distribution Service - edge computing)
![Screenshot from 2023-08-21 15-33-24](https://github.com/Liangyue-1998/ros_learning/assets/61789633/0682937f-05e1-496d-9ad5-1c7801f505f0)
- real time
- Hardware platform indeendence
- Distributed system
- Decoupling
- High extension
  #### Vortex DDS




  














