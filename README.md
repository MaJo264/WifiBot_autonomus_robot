## Wifibot Autonomous Robot Project

In this project, I implemented an autonomous navigation system for the Wifibot robot, using a Raspberry Pi 3 B as the primary controller. The system is designed to navigate from point A to point B autonomously while avoiding obstacles in real-time. The robot is equipped with IR sensors for proximity detection and obstacle avoidance, providing a reliable and cost-effective solution for environmental awareness.

### Objectives

The project had two primary objectives:
1. **Autonomous Navigation**: The robot needed to move from a predefined starting point (Point A) to a destination (Point B) without any human intervention. This was achieved by integrating a custom path planning algorithm with sensor inputs, allowing the robot to dynamically adjust its path in response to the environment.
  
2. **Obstacle Avoidance**: To ensure safe navigation, the robot was equipped with IR sensors that continuously monitor the surroundings for obstacles. When an obstacle is detected, the robot calculates an alternate path to avoid it, ensuring smooth and uninterrupted movement.

### Object Detection

To enhance the robot's capabilities, I integrated YOLOv8 for real-time object detection. This allows the robot to identify and react to various objects in its environment, adding an additional layer of intelligence to the navigation system. YOLOv8 was trained to recognize specific objects relevant to the operating environment, enabling the robot to make informed decisions during its journey.

### Hardware and Software

- **Controller**: Raspberry Pi 3 B board
- **Sensors**: IR sensors for obstacle detection
- **Computer Vision**: YOLOv8 for object detection
- **Software Framework**: Python with ROS (Robot Operating System) for sensor integration and path planning

The modular design of this project allows for easy expansion and upgrading of both hardware and software components, making it adaptable for future enhancements.
