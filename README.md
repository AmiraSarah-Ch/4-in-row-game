Object Detection with Fetch Robot (ROS + OpenCV + Gazebo)
This project simulates a Fetch robot detecting colored objects in a virtual environment using computer vision techniques.

The robot uses its onboard RGB-D camera in a Gazebo simulation to capture real-time images. With the help of ROS (Robot Operating System) and OpenCV, the robot processes these images to identify and locate colored objects based on HSV filtering and masking.

🎥 Demo
<img src="media/demo.gif" align="middle">
🛠️ Installation
✅ Recommended System: Ubuntu 18.04 LTS
✅ ROS version: ROS Melodic

Required Software
ROS Melodic

Gazebo 9

Python 2.7 or 3.x

OpenCV (3.x or 4.x)

cv_bridge (ROS package for OpenCV ↔ ROS image conversion)

Required Dependencies

# Update your system
sudo apt update
sudo apt upgrade

# ROS base dependencies
sudo apt install -y \
  ros-melodic-rospy \
  ros-melodic-std-msgs \
  ros-melodic-sensor-msgs \
  ros-melodic-cv-bridge

# Gazebo integration
sudo apt install -y \
  ros-melodic-gazebo-ros \
  ros-melodic-gazebo-plugins

# OpenCV and general tools
sudo apt install -y \
  python-opencv \
  python-numpy
📂 Project Structure

fetch_object_detection/
├── launch/               # Launch files for Gazebo and camera nodes
├── scripts/              # Python scripts for image processing and detection
├── worlds/               # Custom Gazebo world files
├── config/               # Camera configuration and parameters
├── media/                # Demo images and gifs
└── README.md
🚀 How to Run
Launch the Gazebo environment with the Fetch robot:


roslaunch fetch_object_detection simulation.launch
Start the object detection node:

rosrun fetch_object_detection detect_color.py
A window will open showing the original camera feed and the masked color detection result.

🔍 Features
Real-time image acquisition via RGB-D camera

HSV color filtering to isolate target colors

ROS topic communication for sensor data

Masking and image processing using OpenCV

Easily extendable for object tracking or grasping

📚 Skills Practiced
ROS topic & node management

Image processing (HSV, masking, color detection)

Python scripting with OpenCV

Robotics simulation in Gazebo

📸 Preview

🙌 Credits
Project developed as part of my engineering graduation project (PFE).
Special thanks to my academic supervisor and all mentors involved.

