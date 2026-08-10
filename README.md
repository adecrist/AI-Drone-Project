# Autonomous AI Inspection Drone

## Overview
This repository contains the documentation and milestone planning for a 10-week summer research project developing an AI inspection drone. The system utilizes a Raspberry Pi to process Edge AI vision models in real-time to identify structural defects.

## Current Hardware Architecture
* **Flight Controller/Pixhawk:** Custom implementation using an MPU-6050 Gyro/Accelerometer.
* **Onboard Compute:** Raspberry Pi for Edge AI processing and network telemetry.
* **Power System:** 11.1V (3S) 5000mAh LiPo.
* **Propulsion:** Transitioning to four A2212 1000KV Brushless Motors and matched 12x6E APC propellers (CW/CCW) and 4-30A ESCs
* **Controller/Reciever** FlySky controller/transmitter and FS-iA6B reciever
*  **Camera** ArduCam connected to the raspberry pi through the ribbon

## Repository Contents
* **Week 1 AI Drone Project Presentation:** Slide deck detailing the initial hardware audit, timeline feasibility, and the end goal for the summer
* **Drone Files:** SolidWorks and STL files for the drone parts
* **Drone Project Documentation** Concise description of all of the software and hardware parts from Summer 2025
*  **Wiring Diagram** Brief diagram of how each piece of hardware is connected

## Next Steps
1. Attacth existing hardware to new carbon fiber frame
2. Recallibrate the flight controller on Mission Planner with the new frame
3. Go back to SAS Lab with Prof. Hamid Jafarnejad Sani to test flight

## Live Drone Footage/AI Recognition
1. Connect to the Local Drone Network (PiCam)
2. Verify IP Address by running ipconfig in Windows PowerShell, currently 192.168.4.42
3. In PowerShell type cd "OneDrive\AI Drone Project 2026" ; then python stream.py
4. Connect to Raspberry Pi using ssh terminal
5. Run command: libcamera-vid -t 0 --width 640 --height 480 --framerate 25 --codec h264 --inline --hflip --vflip -o udp://192.168.4.42:5001
6. To shut down press q key on the video feed window and ctrl + c in the raspberry pi terminal

## Connecting to Raspberry Pi
1. Plug in the LiPo battery and connect to PiCam on your laptop
2. Open up command prompt on your computer type in ssh lpan@192.168.4.1 then enter Password Steven27

## Downloading Mission Planner
1. Must have a windows computer
2. Go to the official ArduPilot Mission Planner download directory
3. Click on MissionPlanner-latest.msi for most recent version
4. Go to you downloads to find the file and click it to launch setup wizard
5. Make sure too allow all the pop ups that ask to install device drivers
6. Once installation is complete use the micro-USB cable to connect the Pixhawk to your computer set baud rate to 115200
7. Navigate to Setup then Mandatory Hardware if calibration needs to be done

## Connecting Controller/Transmitter
1. Plug in battery on the drone
2. Hold down the button on the saftey switch(currently have the safety switch turned off), connected to Pixhawk, should hear motor start up sound
3. Turn on the FlySky Transmitter
4. Make sure the throttle is all the way down and the SWA switch if pushed up
5. Bring throttle to the bottom right position until the blue light on the pixhawk is a solid blue
6. Transmitter is then connected
7. To disconnect flick SWA down, then bring throttle to bottom left position until Pixhawk is flashing green

