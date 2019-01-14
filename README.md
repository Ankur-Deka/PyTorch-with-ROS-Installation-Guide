# Anaconda-with-ROS-Installation-Guide
Get Anaconda and ROS running together on Ubuntu 16.04

1. Install Anaconda: https://conda.io/docs/user-guide/install/linux.html

1. Set default python version to python 2.7
   1. conda update conda
   1. conda install python=2.7

1. Install ROS
   (Skip i,ii if ROS was installed earlier)
   1. sudo -E sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
   1. sudo -E apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
   1. sudo apt-get update
   1. sudo apt-get install ros-kinetic-desktop-full

1. Install catkin_pkg
   1. conda install -c auto catkin_pkg 

1. Install extra dependencies
   1. pip install -U rosdep rosinstall_generator wstool rosinstall six vcstools
   1. pip install msgpack
   1. pip install empy
   DONT: pip install em - it confuses em for empy and catkin_make doesn’t work

1. Source it:
   1. source /opt/ros/kinetic/setup.bash
