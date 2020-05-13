## Open Manipulator x
### use ROS1

```
$ sudo apt install ros-melodic-controller-* ros-melodic-gazebo-* ros-melodic-moveit* ros-melodic-industrial-core 
$ mkdir -p catkin_ws/src
$ cd ~/catkin_ws/src/
$ git clone https://github.com/ROBOTIS-GIT/DynamixelSDK.git
$ git clone https://github.com/ROBOTIS-GIT/dynamixel-workbench.git
$ git clone https://github.com/ROBOTIS-GIT/dynamixel-workbench-msgs.git
$ git clone https://github.com/ROBOTIS-GIT/open_manipulator.git
$ git clone https://github.com/ROBOTIS-GIT/open_manipulator_msgs.git
$ git clone https://github.com/ROBOTIS-GIT/open_manipulator_simulations.git
$ git clone https://github.com/ROBOTIS-GIT/robotis_manipulator.git

$ sudo apt install python-catkin-tools 
$ cd ~/catkin_ws/ && catkin build
```

```
$ source ~/catkin_ws/devel/setup.bash
$ roslaunch open_manipulator_gazebo open_manipulator_gazebo.launch 

$ roslaunch open_manipulator_controller open_manipulator_controller.launch
$ roslaunch open_manipulator_teleop open_manipulator_teleop_keyboard.launch
```

- Keyboard teleop
  - srv : goal_task_space_path_from_present_position_only

``` 
$ roscore
$ rosrun open_manipulator_controller create_udev_rules

$ roslaunch open_manipulator_controller open_manipulator_controller.launch
$ roslaunch open_manipulator_teleop open_manipulator_teleop_keyboard.launch
```
---------------------------------------------------------------------------
open_manipulator_gazebo

  - config/open_manipulator_controller.yaml
    - joint_state_publisher
      - Publish all joint states
    
    - joint?_position
      - joint_position_controller  

---------------------------------------------------------------------------

### use ROS2

```
$ sudo apt install python3-rospkg
$ sudo apt install ros-dashing-python* ros-dashing-rqt*
$ mkdir -p ~/robotis_ws/src/ && cd ~/robotis_ws/src
$ git clone -b ros2 https://github.com/ROBOTIS-GIT/DynamixelSDK.git
$ git clone -b ros2 https://github.com/ROBOTIS-GIT/dynamixel-workbench.git
$ git clone -b ros2 https://github.com/ROBOTIS-GIT/open_manipulator.git 
$ git clone -b ros2 https://github.com/ROBOTIS-GIT/open_manipulator_msgs.git
$ git clone -b ros2 https://github.com/ROBOTIS-GIT/open_manipulator_dependencies.git
$ git clone -b ros2 https://github.com/ROBOTIS-GIT/robotis_manipulator.git

$ cd ~/robotis_ws && colcon build --symlink-install
```

```
$ source ~/robotis_ws/install/local_setup.bash 
$ ros2 run open_manipulator_x_controller create_udev_rules 
$ ros2 launch open_manipulator_x_controller open_manipulator_x_controller.launch.py 
```

```
$ source ~/robotis_ws/install/local_setup.bash 
$ ros2 topic pub /open_manipulator_x/option std_msgs/msg/String "data: print_open_manipulator_x_setting"
$ ros2 run open_manipulator_x_teleop open_manipulator_x_teleop_keyboard
```

- gripper
  - srv (open_manipulator_msgs::srv::SetJointPosition)
    - open_manipulator_x/goal_tool_control
   
    - joint_name: gripper
    - position: 0.01(open) or -0.01(close)