# Autonomous AI Inspection Drone

## Overview
This repository contains the documentation and milestone planning for a 10-week summer research project developing an AI inspection drone. The system utilizes a Raspberry Pi to process Edge AI vision models in real-time to identify structural defects.

## Current Hardware Architecture
* **Flight Controller:** Custom implementation using an MPU-6050 Gyro/Accelerometer.
* **Onboard Compute:** Raspberry Pi for Edge AI processing and network telemetry.
* **Power System:** 11.1V (3S) 5000mAh LiPo.
* **Propulsion Upgrade (In Progress):** Transitioning to four A2212 1000KV Brushless Motors and matched 12x6E APC propellers (CW/CCW) to resolve a low-end torque deficit and prevent ESC overload.

## Repository Contents
* **Week 1 AI Drone Project Presentation:** Slide deck detailing the initial hardware audit, timeline feasibility, and the end goal for the summer
* **Drone Files:** SolidWorks and STL files for the drone parts
* **Drone Project Documentation** Concise description of all of the software and hardware parts from Summer 2025

## Next Steps
1. Procure and install the 1000KV motors and 12-inch blades.
2. Manufacture the structural clamp and mount the MPU-6050 sensor at the chassis center of gravity.
3. Establish connection to the Raspberry Pi and connect to the video camera

## Live Drone Footage Steps
1. Connect to the Local Drone Network
2. Verify IP Address by running ipconfig in Windows PowerShell, currently 192.168.4.42
3. In PowerShell type cd "OneDrive\AI Drone Project 2026" ; then python stream.py
4. Connect to Raspberry Pi using ssh terminal
5. Run command: libcamera-vid -t 0 --width 640 --height 480 --framerate 25 --codec h264 --inline --hflip --vflip -o udp://192.168.4.42:5001
6. To shut down press q key on the video feed window and ctrl + c in the raspberry pi terminal
