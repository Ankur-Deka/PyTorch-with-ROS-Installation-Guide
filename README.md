# Anaconda-with-ROS-Installation-Guide
Get Anaconda and ROS running together on Ubuntu 16.04

1. Install Anaconda: https://docs.anaconda.com/anaconda/install/linux/

1. Set default python version to python 2.7
```shell
 conda update conda
 conda install python=2.7
```
1. Install ROS
   (Skip first 2 lines if ROS was installed earlier)
```shell
sudo -E sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
sudo -E apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
sudo apt-get update
sudo apt-get install ros-kinetic-desktop-full
```
1. Install rospkg and catkin_pkg
```shell
conda install -c conda-forge rospkg catkin_pkg 
```
1. Install extra dependencies
```shell
sudo apt install python-rosdep
conda install pip
pip install -U rosinstall_generator wstool rosinstall six vcstools msgpack empy
```
DONT: `pip install em` - it confuses em for empy and catkin_make doesn’t work
1. Source it:
   1. `source /opt/ros/kinetic/setup.bash`
   1. For sourcing permanently: `sudo gedit ~/.bashrc` and add the above line to the end of the file. Then run `source ~/.bashrc`
1. Intitialize rosdep:
```shell
sudo rosdep init
rosdep update
```
