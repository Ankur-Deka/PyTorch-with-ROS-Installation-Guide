# Anaconda-with-ROS-Installation-Guide
Get Anaconda and ROS running together on Ubuntu 16.04

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b

1. Install Anaconda: https://conda.io/docs/user-guide/install/linux.html

1. Set default python version to python 2.7
  1. conda update conda
  1. conda install python=2.7

3) Install ROS

  (Skip a,b if ROS was installed earlier)

  a) sudo -E sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

  b) sudo -E apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116

  c) sudo apt-get update

d) sudo apt-get install ros-kinetic-desktop-full

4) Install catkin_pkg

a) conda install -c auto catkin_pkg 

5) Install extra dependencies

a) pip install -U rosdep rosinstall_generator wstool rosinstall six vcstools

b) pip install msgpack

c) pip install empy

DONT: pip install em - it confuses em for empy and catkin_make doesn’t work

6) Source it:

a) source /opt/ros/kinetic/setup.bash
