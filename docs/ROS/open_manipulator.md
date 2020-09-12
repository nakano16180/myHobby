## Open Manipulator x

### use ROS1 (Melodic)

```
$ sudo apt install ros-melodic-desktop-full
$ sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

```

#### use catkin-tools

```
$ sudo apt install python-catkin-tools
```

#### install dependencies

```
$ sudo apt install ros-melodic-controller-* ros-melodic-gazebo-* ros-melodic-moveit* ros-melodic-industrial-core
```

#### install packages and build

```
$ mkdir -p catkin_ws/src
$ cd ~/catkin_ws/src/
$ git clone https://github.com/ROBOTIS-GIT/DynamixelSDK.git
$ git clone https://github.com/ROBOTIS-GIT/dynamixel-workbench.git
$ git clone https://github.com/ROBOTIS-GIT/dynamixel-workbench-msgs.git
$ git clone https://github.com/ROBOTIS-GIT/open_manipulator.git
$ git clone https://github.com/ROBOTIS-GIT/open_manipulator_msgs.git
$ git clone https://github.com/ROBOTIS-GIT/open_manipulator_simulations.git
$ git clone https://github.com/ROBOTIS-GIT/robotis_manipulator.git

$ cd ~/catkin_ws/ && catkin build
```

#### launch Gazebo simulator

- [Gazebo Simlation](http://emanual.robotis.com/docs/en/platform/openmanipulator_x/ros_simulation/)
- [Operation](http://emanual.robotis.com/docs/en/platform/openmanipulator_x/ros_operation/)

```
$ source ~/catkin_ws/devel/setup.bash
$ roslaunch open_manipulator_gazebo open_manipulator_gazebo.launch

$ roslaunch open_manipulator_controller open_manipulator_controller.launch
$ roslaunch open_manipulator_teleop open_manipulator_teleop_keyboard.launch
```

#### launch real robot

```
$ roscore
$ rosrun open_manipulator_controller create_udev_rules

$ roslaunch open_manipulator_controller open_manipulator_controller.launch
$ roslaunch open_manipulator_teleop open_manipulator_teleop_keyboard.launch
```

### use ROS2

#### install dependencies

```
$ sudo apt install python3-rospkg
$ sudo apt install ros-dashing-python* ros-dashing-rqt*
```

#### install packages and build

```
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
```

```
$ source ~/robotis_ws/install/local_setup.bash
$ ros2 launch open_manipulator_x_controller open_manipulator_x_controller.launch.py
```

```
$ source ~/robotis_ws/install/local_setup.bash
$ ros2 topic pub /open_manipulator_x/option std_msgs/msg/String "data: print_open_manipulator_x_setting"
$ ros2 run open_manipulator_x_teleop open_manipulator_x_teleop_keyboard
```
