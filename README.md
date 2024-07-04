# How to install Ros noetic:

## Set up your sources list
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-noetic.list'

## Add the ROS GPG key
sudo apt install curl
curl -sSL 'https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc' | sudo apt-key add -

## Update your package index
sudo apt update

## Install ROS Noetic
sudo apt install ros-noetic-desktop-full

## Set up your environment
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

## Install rosinstall and other development tools
sudo apt install python3-rosinstall python3-rosinstall-generator python3-wstool build-essential

## install rosdep
sudo apt install python3-rosdep

## initialize rosdep
sudo apt install python3-rosdep
sudo rosdep init
rosdep update

## Verify your installation
roscore
