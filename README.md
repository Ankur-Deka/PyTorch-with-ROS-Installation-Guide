# Anaconda-with-ROS-Installation-Guide
Get Anaconda and ROS running together on Ubuntu 16.04

Set default python version to python 2.7
conda update conda
conda install python=2.7
Install ROS again
(Skip a,b if ROS was installed earlier)
sudo -E sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
sudo -E apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
sudo apt-get update
sudo apt-get install ros-kinetic-desktop-full
Install catkin_pkg
conda install -c auto catkin_pkg 
Install extra dependencies
pip install -U rosdep rosinstall_generator wstool rosinstall six vcstools
pip install msgpack
pip install empy
DONT: pip install em - it confuses em for empy and catkin_make doesn’t work
Source it:
source /opt/ros/kinetic/setup.bash
