# ROS2-Humble-Hawksbill
Installing ROS2 Humble Hawksbill on 22.04


1-nstall Ubuntu mate 20.04
from the following link:

https://releases.ubuntu-mate.org/20.04/amd64/


2-open the terminal to write the ROS 2 installation commands.

1-Set Locale:
```
locale  # check for UTF-8

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings
```


2- Setup Sources:
```
apt-cache policy | grep universe or

sudo apt install software-properties-common

sudo add-apt-repository universe

sudo apt update && sudo apt install curl -y
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

```
3 - Installing ROS packages:
```
sudo apt update
sudo apt upgrade
sudo apt install ros-humble-desktop
sudo apt install ros-humble-ros-base
```
4 - Environment Setup:
```
source /opt/ros/humble/setup.bash
```

Get the commands from here: https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html#environment-setup
