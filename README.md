# HANUMA Autonomous Mine Safety Rover

A rugged autonomous underground mine inspection and rescue rover designed for hazard detection, environmental monitoring, navigation, and remote situational awareness in GPS-denied, low-visibility mine environments.

## Overview

HANUMA is a six-wheel rocker-bogie robotic platform built for autonomous operation in hazardous underground conditions. The rover combines ROS 2 navigation, LiDAR mapping, 3D perception, IMU and odometry fusion, gas monitoring, long-range LoRa communication, and a live telemetry dashboard into a unified mine-safety inspection system.

The platform is intended for:
- autonomous exploration and mapping in underground corridors
- obstacle avoidance and path planning in cluttered terrain
- hazard awareness through gas, dust, and environmental sensing
- operator visibility through a real-time dashboard
- rescue support and pre-entry reconnaissance in risky mining zones
- robust operation in GPS-denied and RF-constrained environments

## Core Technologies

### Autonomous Robotic Stack
- ROS 2 navigation and control framework
- SLAM and localization pipeline for GPS-denied operation
- Nav2-based path planning and obstacle avoidance
- IMU + wheel odometry + LiDAR fusion
- 3D camera / depth perception for environment understanding
- rugged six-wheel rocker-bogie mobility platform

### Perception and Sensing
- 2D LiDAR for obstacle detection and map generation
- 3D camera and vision sensors for scene interpretation
- HD / IR camera for low-light and dusty visibility conditions
- ultrasonic sensing for proximity detection
- gas sensor array for CH4, CO, CO2, O2, H2S
- dust, humidity, and environmental sensing
- vibration or acoustic sensing for structure-awareness support

### Embedded and Hardware Layer
- ESP32-based low-level control and sensor acquisition
- motor control and safety logic
- modular chassis design for sensor integration
- robust electrical architecture for field deployment scenarios

### Communication and Resilience
- LoRa-based communication for long-range and low-power telemetry
- breadcrumb / relay-style communication concept for degraded RF environments
- mission-state reporting to a remote operator dashboard
- failsafe logic for communication loss and safe return behavior

## System Architecture

HANUMA follows a split-compute architecture:

- Low-level layer: ESP32 for motor control, sensor reading, and hardware safety
- High-level layer: Raspberry Pi 5 for ROS 2, SLAM, perception, and navigation
- Data layer: sensor fusion, mapping, telemetry, and dashboard communication
- Operator layer: remote dashboard with environmental data and rover state

## Why HANUMA Matters

Underground mines are dangerous environments with poor visibility, toxic gases, unstable ground, and limited communication. Traditional inspection methods expose humans to significant risk. HANUMA reduces that risk by enabling autonomous scouting, monitoring, and mapping before human intervention.

## Repository Organization

```text
HANUMA/
├── README.md
├── REPORT.md
├── .gitignore
├── HANUMA_DASHBOARD.html
├── HANUMA.txt
├── HANUMA_Mine_Data_2026-07-30T06-43-49.csv
├── HANUMA_Mine_Data_2026-08-06T05-41-57.csv
├── HANUMA_Mine_Data_2026-08-21T12-24-45.csv
├── HANUMA_Patent_Full.docx
├── HANUMA_Robotic_Mine_Safety.pptx
├── HANUMA_Robotic_Mine_Safety (2).pdf
├── IDEA.pdf
├── IDEA.pptx
├── Patent Report.pdf
├── Patent Report.docx
├── Project HANUMA Master Prompt.pdf
├── PNT Lab - Final Report ...docx
├── docs/
│   ├── README.md
│   ├── images/
│   └── reports/
├── firmware/
│   └── README.md
├── ros2_ws/
│   └── README.md
├── edge_ai/
│   └── README.md
├── dashboard/
│   └── README.md
├── simulation/
│   └── README.md
├── data/
│   └── README.md
└── .github/
    └── workflows/
```

## Project Highlights

- ROS 2 autonomous navigation
- LiDAR-based environment mapping
- 3D vision and scene understanding
- collision avoidance and path planning
- gas and environmental hazard detection
- rugged mine-ready platform
- LoRa communication for harsh RF conditions
- live dashboard telemetry and monitoring
- modular embedded robotics architecture

## GitHub Presentation Strategy

For a professional GitHub repository:
- `README.md` is the landing page
- `REPORT.md` contains the technical project documentation
- `docs/` stores presentations, PDFs, architecture files, and screenshots
- source folders hold the software and system assets
- CSV logs and telemetry files are preserved for traceability

## Push Commands

```bash
git add .
git commit -m "feat: final HANUMA autonomous mine safety rover update"
git push origin main
```

## Summary

HANUMA represents a complete autonomous robotic solution for underground mine safety. It integrates robotics, embedded systems, AI perception, mapping, navigation, long-range communication, and remote telemetry to address critical operational challenges in mine inspection and rescue scenarios.
