# 🐢 Turtlesim Basic Commands (ROS2 Humble)

## Launch turtlesim
```bash
ros2 run turtlesim turtlesim_node
```

## Control with keyboard
```bash
ros2 run turtlesim turtle_teleop_key
```

## Publish velocity command
```bash
ros2 topic pub /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0}, angular: {z: 1.5}}"
```

## View topics
```bash
ros2 topic list
```

## Echo turtle position
```bash
ros2 topic echo /turtle1/pose
```

## Teleport turtle
```bash
ros2 service call /turtle1/teleport_absolute turtlesim/srv/TeleportAbsolute "{x: 3.0, y: 3.0, theta: 0.0}"
```

## Clear background
```bash
ros2 service call /clear std_srvs/srv/Empty
```