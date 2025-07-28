# 🛠️ ROS2 Humble Setup on Ubuntu 22.04

## 1. System Update
```bash
sudo apt update && sudo apt upgrade
```

## 2. Install Required Tools
```bash
sudo apt install curl gnupg2 lsb-release
```

## 3. Add ROS2 Repository
```bash
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
sudo sh -c 'echo "deb http://packages.ros.org/ros2/ubuntu $(lsb_release -cs) main" > /etc/apt/sources.list.d/ros2-latest.list'
```

## 4. Install ROS2 Humble
```bash
sudo apt update
sudo apt install ros-humble-desktop
```

## 5. Source ROS2
```bash
echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
source ~/.bashrc
```