## ignition

- [ドキュメントページ](https://ignitionrobotics.org/docs)
- 次世代 Gazebo

## Setup

- [ここ](https://products.rt-net.jp/micromouse/archives/8764)が分かりやすい
- [公式のインストールドキュメント](https://ignitionrobotics.org/docs/citadel)
- [ROS1 との連携](https://ignitionrobotics.org/docs/citadel/ros_integration)
- [Gazebo との比較](https://ignitionrobotics.org/docs/citadel/comparison)
  - まだ移行が進んでないプラグインもわりとある

## source

- [Ignition Robotics(github)](https://github.com/ignitionrobotics/)
- [公式リポジトリ](https://github.com/ignitionrobotics/ign-gazebo)
  - [Ignition で使えるプラグイン 1](https://github.com/ignitionrobotics/ign-gazebo/tree/master/include/ignition/gazebo/components)
  - [Ignition で使えるプラグイン 2](https://github.com/ignitionrobotics/ign-gazebo/tree/master/src/systems)
  - [ign-gazebo/example/worlds](https://github.com/ignitionrobotics/ign-gazebo/tree/master/examples/worlds)

### example

- [Ignition+ROS Melodic で走らせる Raspberry Pi Mouse](https://products.rt-net.jp/micromouse/archives/8833)
  - [ソースリポジトリ](https://github.com/Tiryoh/ros_ign_gazebo_raspimouse)
- [example/worlds/diff_dlive.sdf](https://bitbucket.org/ignitionrobotics/ign-gazebo/src/default/examples/worlds/diff_drive.sdf)
  - [プラグイン](https://bitbucket.org/ignitionrobotics/ign-gazebo/src/default/src/systems/diff_drive/)

## install ros_ign

```
$ source ~/catkin_ws/devel/setup.bash
$ cd ~/catkin_ws/src/
$ git clone https://github.com/osrf/ros_ign.git -b melodic

$ export IGNITION_VERSION=citadel
$ rosdep install --from-paths src -i -y --rosdistro melodic \
  --skip-keys=ignition-gazebo2 \
  --skip-keys=ignition-gazebo3 \
  --skip-keys=ignition-msgs4 \
  --skip-keys=ignition-msgs5 \
  --skip-keys=ignition-rendering2 \
  --skip-keys=ignition-rendering3 \
  --skip-keys=ignition-sensors2 \
  --skip-keys=ignition-sensors3 \
  --skip-keys=ignition-transport7 \
  --skip-keys=ignition-transport8

$ source ~/catkin_ws/devel/setup.bash
$ cd ~/catkin_ws/ && catkin build
$ roslaunch open_manipulator_ign open_manipulator_ign.launch

```
