# Adaptive-Monte-Carlo-Localization-in-ROS
## Introduction
Monte Carlo Localization is an algorithm for robots to localize using a particle filter, Given a map of the environment, the algorithm estimates the position and orientation of a robot as it moves and senses the environment, however in this project we are using Adaptive Monte Carlo Localization in our purposes, (AMCL) dynamically adjusts the number of particles over a period of time, as the robot navigates around in a map. This adaptive process offers a significant computational advantage over MCL.

![Before_Tuning_Default_Values_1](https://user-images.githubusercontent.com/105011124/168918147-45060592-e5b3-42ed-a4b4-c5fd5cfc0ac1.PNG)

## Localization Test
place ```amcl.launch``` file in your robot's launch folder,
### 1. Launch the robot inside your world
```bash
$ cd /home/workspace/catkin_ws/
$ source devel/setup.bash
$ roslaunch my_robot world.launch
```
### 2. Run ```amcl``` packge
```bash
$ cd /home/workspace/catkin_ws/
$ source devel/setup.bash
$ roslaunch my_robot amcl.launch
```
### 3. Move your robot
use ```ros-teleop``` package to send command to the robot using keyboard or controller,
#### - Clone the ```ros-teleop``` package to your ```src``` folder:
```bash
$ cd /home/workspace/catkin_ws/src
$ git clone https://github.com/ros-teleop/teleop_twist_keyboard
```
#### - Run the ```teleop``` script
```bash
$ rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```
### 4. Preview
This is a preview video of robot's localization using amcl package, [Click here](https://www.youtube.com/watch?v=fFR2rek36js)



