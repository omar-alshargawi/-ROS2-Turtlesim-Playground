# 🐢 ROS2 Turtlesim Control (Ubuntu 22.04 + Humble)

A beginner-friendly project to install and run the `turtlesim` simulation package in **ROS2 Humble** using **Ubuntu 22.04**.  
The project introduces basic ROS2 concepts like **nodes**, **topics**, **services**, and **commands** through the iconic turtle robot.

---

## 🎯 Project Goal

Learn how to:
- Set up ROS2 Humble on a virtual machine (Ubuntu 22.04)
- Understand and control nodes in a ROS2 system
- Publish velocity commands to move the turtle
- Use services to teleport, reset, or clear the turtle environment
- Work in a real terminal-based robotics environment

---

## 🧱 What We Did

We created a virtualized ROS2 environment using VirtualBox and Ubuntu 22.04.

Inside that, we:
1. Installed **ROS2 Humble** with all dependencies  
2. Ran the **turtlesim_node** to launch the turtle GUI  
3. Used terminal commands to:
   - Move the turtle with velocity topics
   - Teleport it using services
   - Listen to its pose via topics
   - Control it manually via keyboard

---

## 🛠️ Tools & Technologies  

- 🐢 ROS2 Humble  
- 💻 Ubuntu 22.04 (via VirtualBox)  
- 🔑 Terminal CLI  
- 🧠 Topics, Nodes, Services (core ROS2 concepts)

---

## 🚦 How It Works

### 1. Run the turtle simulator:

```bash
ros2 run turtlesim turtlesim_node
```

### 2. Control the turtle with keyboard:

```bash
ros2 run turtlesim turtle_teleop_key
```

### 3. View active topics:

```bash
ros2 topic list
```

### 4. Echo turtle pose:

```bash
ros2 topic echo /turtle1/pose
```

### 5. Send velocity command:

```bash
ros2 topic pub /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0}, angular: {z: 1.5}}"
```

### 6. Call teleport service:

```bash
ros2 service call /turtle1/teleport_absolute turtlesim/srv/TeleportAbsolute "{x: 4.0, y: 2.0, theta: 1.0}"
```

---

## 💡 Tips

You must source ROS2 in each new terminal:

```bash
source /opt/ros/humble/setup.bash
```

To reset the simulator:

```bash
ros2 service call /clear std_srvs/srv/Empty
```

---

## 🚀 Setup Guide

```bash
# 1) Install VirtualBox & Ubuntu 22.04
# 2) Inside Ubuntu, install ROS2:
sudo apt update && sudo apt install curl gnupg2 lsb-release

# 3) Follow official ROS2 Humble install steps:
https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html

# 4) Run turtlesim as above
```

---

## 📸 Project Review
![preview](https://github.com/user-attachments/assets/d6e5b097-a212-4fcb-946a-cb2c608f2c2b)

---

## 👤 Author
> Designed by: **Omar Alshargawi**  
> Date: **28 Jul 2025**
