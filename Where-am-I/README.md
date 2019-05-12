
# Where Am I?
## Overview 
The goal of this project is accurately localize a mobile robot inside a provided map in the Gazebo and RViz simulation environments.
For this purpose, the following tasks were performed:
* Building a mobile robot for simulated tasks.
* Creating a ROS package that launches a custom robot model in a Gazebo world and utilizes packages like AMCL and the Navigation Stack.
* Exploring, adding, and tuning specific parameters corresponding to each package to achieve the best possible localization results.

[image_0]: https://github.com/BrunoEduardoCSantos/Where-am-I/blob/master/images/start.png
![alt text][image_0] 

[image_1]: https://github.com/BrunoEduardoCSantos/Where-am-I/blob/master/images/goal.png
![alt text][image_1] 

## Installation Instructions

This project requires a Ubuntu System with ROS Kinetic installed on it. Some specific ROS packages might be required in order to install this ROS package:

``` bash
$ sudo apt-get install ros-kinetic-navigation
$ sudo apt-get install ros-kinetic-map-server
$ sudo apt-get install ros-kinetic-move-base
$ rospack profile
$ sudo apt-get install ros-kinetic-amcl
```

 
## Run the Project

After completing the project, you can launch it by running the following commands first -

```bash
$ cd ~/catkin_ws
$ catkin_make
$ source devel/setup.bash
```

And then run the following in *separate* terminals -

``` bash
$ roslaunch udacity_bot udacity_bot
$ roslaunch udacity_bot amcl
$ rosrun udacity_bot navigation goal
```
