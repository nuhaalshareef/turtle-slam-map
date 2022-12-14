# turtle-slam-map 
First we visit turtlebot3 website " TurtleBot3 (robotis.com) " , and change the vision to noetic .then we follow the steps:
# Install Dependent ROS Packages
```
$ sudo apt-get install ros-kinetic-joy ros-kinetic-teleop-twist-joy \
  ros-kinetic-teleop-twist-keyboard ros-kinetic-laser-proc \
  ros-kinetic-rgbd-launch ros-kinetic-depthimage-to-laserscan \
  ros-kinetic-rosserial-arduino ros-kinetic-rosserial-python \
  ros-kinetic-rosserial-server ros-kinetic-rosserial-client \
  ros-kinetic-rosserial-msgs ros-kinetic-amcl ros-kinetic-map-server \
  ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro \
  ros-kinetic-compressed-image-transport ros-kinetic-rqt* \
  ros-kinetic-gmapping ros-kinetic-navigation ros-kinetic-interactive-markers
  ```
  # Install TurtleBot3 Packages
  ```
 $ sudo apt-get install ros-kinetic-dynamixel-sdk
$ sudo apt-get install ros-kinetic-turtlebot3-msgs
$ sudo apt-get install ros-kinetic-turtlebot3
```
# Install Simulation Package
```
$ cd ~/catkin_ws/src/
$ git clone -b kinetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make
```
# Operate TurtleBot3
```
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
# Launch Simulation World
```
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
# Run SLAM Node
```
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```
![unnamed (5)](https://user-images.githubusercontent.com/108008564/183267316-602b8544-21f1-4879-aebf-ae2260946daf.jpg)

# Run Teleoperation Node
```
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
#  Control Your TurtleBot3!
```
 Moving around:
        w
   a    s    d
        x

 w/x : increase/decrease linear velocity
 a/d : increase/decrease angular velocity
 space key, s : force stop
 ```
 ![unnamed (6)](https://user-images.githubusercontent.com/108008564/183267335-c2185aad-c4f2-4f2c-b82d-967eda85538f.jpg)

