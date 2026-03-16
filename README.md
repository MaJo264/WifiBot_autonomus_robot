# 🧭 WiFiBot — Autonomous Navigation Robot

Full autonomy stack on a Raspberry Pi — real-time object detection, obstacle avoidance, and path planning in a modular ROS architecture. Python and C++ on resource-constrained embedded hardware.

![C++](https://img.shields.io/badge/C++-97%25-blue) ![Python](https://img.shields.io/badge/Python-3.8+-yellow) ![ROS](https://img.shields.io/badge/Framework-ROS-brightgreen) ![YOLOv8](https://img.shields.io/badge/Detection-YOLOv8-green) ![Platform](https://img.shields.io/badge/Platform-Raspberry%20Pi%203B-red)

## 📌 Overview
WiFiBot is an autonomous ground robot built on the **Wifibot** platform, controlled by a **Raspberry Pi 3B**. The system navigates from a start point to a destination entirely autonomously — detecting and avoiding obstacles in real time using IR sensors and YOLOv8-based object detection. Built as part of an MSc in Automotive Embedded Systems (ESIGELEC, Rouen).

## 🎯 Features

**Autonomous Navigation (A → B)** — Custom path planning algorithm integrated with sensor inputs. Navigates to a destination without human intervention, dynamically adjusting its path in response to the environment.

**Real-Time Obstacle Avoidance** — IR sensors continuously monitor the surroundings. When an obstacle is detected, the system calculates an alternate path and adjusts heading in real time.

**Deep Learning Object Detection** — YOLOv8 runs on the Raspberry Pi camera feed to identify and classify objects — adding an intelligence layer on top of IR-based proximity detection.

## 🛠️ Tech Stack

| Component | Technology |
|-----------|------------|
| Object Detection | YOLOv8 |
| Robot Framework | ROS |
| Primary Language | C++ |
| Vision & ML | Python |
| Controller | Raspberry Pi 3B |
| Sensors | IR Proximity Sensors |

## 📁 Repository Structure

```
├── main.cpp              # Main robot control loop
├── WifibotClient.cpp     # Motor control interface
├── WifibotClient.h       # WiFiBot client header
├── cam.py                # Camera feed + YOLOv8 detection
└── README.md
```

## ⚙️ Setup & Installation
```bash
# Python dependencies
pip install ultralytics opencv-python numpy

# Build C++ components
g++ -o wifibot_control main.cpp WifibotClient.cpp -std=c++17

# Run
roscore
python3 cam.py
./wifibot_control
```

## 📊 Results

- ✅ Autonomous A→B navigation validated on real hardware
- ✅ Real-time obstacle avoidance using IR sensors
- ✅ YOLOv8 object detection on Raspberry Pi camera feed
- ✅ Modular C++/Python architecture — clean separation between perception, planning, and control

## 🔮 Future Work

- Migrate to ROS2 for improved real-time performance
- Integrate SLAM for map-based localisation
- Add Deep SORT multi-object tracking
- Deploy TensorRT-optimised YOLOv8 for faster edge inference

## 👤 Author

**Avin Joseph** — MSc Automotive Embedded Systems, ESIGELEC Rouen  
[LinkedIn](https://linkedin.com/in/avin-joseph) · [GitHub](https://github.com/MaJo264)
