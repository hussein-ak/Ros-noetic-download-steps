# How to install Ros noetic:
- install virtual machine
- install ubuntu 20.04 and link it to your virtual machine
- open a terminal and start writing the code below

## Set up your sources list
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-noetic.list'

## Add the ROS GPG key
- sudo apt install curl
- curl -sSL 'https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc' | sudo apt-key add -

## Update your package index
sudo apt update


## Install ROS Noetic
sudo apt install ros-noetic-desktop-full


## Set up your environment
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

## output of the above codes
![image](https://github.com/hussein-ak/Ros-noetic-download-steps/assets/173874366/0dca7a3a-679d-4764-b975-aa101f65296f)


## Install rosinstall and other development tools
sudo apt install python3-rosinstall python3-rosinstall-generator python3-wstool build-essential


## install rosdep
sudo apt install python3-rosdep


## initialize rosdep
sudo apt install python3-rosdep
sudo rosdep init
rosdep update

## output of the above codes
![image](https://github.com/hussein-ak/Ros-noetic-download-steps/assets/173874366/30a9af64-717f-4cc6-a484-4b46543f7060)


## Verify your installation
roscore


## image of the output
<img width="564" alt="image" src="https://github.com/hussein-ak/Ros-noetic-download-steps/assets/173874366/22e950c5-80b2-4810-a585-6a513c113ec5">

### what it contains
- The output noetic when running rosversion -d.
- ROS environment variables are listed when running printenv | grep ROS.
- ROS master node running when running roscore.


