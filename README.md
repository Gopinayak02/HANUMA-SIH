# HANUMA Autonomous Mine Safety Rover

A rugged autonomous underground mine inspection and rescue robot built for navigation, hazard detection, environmental monitoring, and remote situational awareness in GPS-denied and low-visibility mine environments.

## Project Overview

HANUMA is a six-wheel rocker-bogie rover designed to operate in hazardous underground conditions with minimal human intervention. The platform combines ROS 2 autonomy, LiDAR-based mapping, IMU and odometry fusion, 3D perception, gas sensing, LoRa communication, and a live telemetry dashboard to perform terrain navigation, hazard detection, and environmental monitoring.

The system is designed for:
- Autonomous exploration and mapping in underground corridors
- Obstacle avoidance and path planning in cluttered environments
- Gas, dust, humidity, and environmental monitoring
- Remote operator visualization through a dashboard
- Rescue support operations in GPS-denied mine conditions
- Reliable communication in RF-attenuated and partially disconnected environments

## Core System Architecture

### Perception and Sensing
- 2D LiDAR for obstacle detection and mapping
- 3D depth camera / vision sensor for scene understanding and object recognition
- IMU for attitude estimation and stabilization
- Wheel odometry for motion estimation
- Gas and air-quality sensors for CH4, CO, CO2, O2, H2S, dust, humidity
- Acoustic / vibration sensing for structure and collapse awareness
- HD or IR camera for low-light and dusty inspection

### Compute Stack
- Raspberry Pi 5 as the high-level autonomy computer
- ROS 2 for robot control, navigation, sensor drivers, and data orchestration
- SLAM and localization stack for GPS-denied navigation
- Nav2 navigation framework for path planning and obstacle avoidance
- Edge AI inference for object and hazard detection
- ESP32 for low-level hardware control, sensor acquisition, and safety logic

### Mobility and Hardware
- Six-wheel rocker-bogie chassis
- Stable traction over rough terrain
- Designed for uneven mine floors and obstacle negotiation
- Modular robotic frame for sensor integration and rapid development

### Communication and Resilience
- LoRa for long-range, low-power communication
- Multi-hop / breadcrumb-style communication concepts for constrained environments
- Telemetry streaming to a dashboard and cloud or local monitoring workstation
- Failsafe return-to-communication behavior if signal is lost

## Autonomous Navigation and Intelligence

HANUMA integrates a multi-layer autonomy stack for underground deployment:

- Localization: fused wheel odometry + IMU + LiDAR-based environmental constraints
- Mapping: occupancy and terrain representation for navigation
- Planning: ROS 2 Nav2 planners and local/global cost maps
- Obstacle avoidance: LiDAR and camera-based perception
- Hazard detection: AI-assisted visual analysis and environmental alerting
- Operator visibility: dashboard with live map, telemetry, gas trends, and rover state

## Technical Highlights

- ROS 2 autonomous robot software stack
- LiDAR-based mapping and navigation
- 3D camera perception for mine scene understanding
- Real-time gas and environmental monitoring
- LoRa-based communication for harsh environments
- Modular embedded hardware design using ESP32
- Dashboard for remote command visibility and telemetry
- Rover platform tailored for rough terrain and unsafe environments

## Repository Structure

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
├── PNT Lab - Final Report _ B Venkat Gopi Nayak & M Bindu Madhavi.docx
├── docs/
│   ├── README.md
│   ├── presentations/
│   ├── reports/
│   └── images/
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

## Recommended GitHub Upload Structure

```text
HANUMA_SIH2026/
├── firmware/                 # ESP32 control and embedded logic
├── ros2_ws/                  # ROS 2 navigation, SLAM, drivers, launch files
├── edge_ai/                  # YOLO and vision / hazard detection scripts
├── dashboard/                # HTML/JS dashboard and live telemetry interface
├── simulation/               # Gazebo/Webots worlds, config, scripts
├── docs/                     # PDFs, presentations, manuals, screenshots
├── data/                     # logs, CSV, telemetry, mission data
├── REPORT.md
├── README.md
├── .gitignore
└── LICENSE (optional)
```

## Project Documents Included

- `HANUMA_DASHBOARD.html` — live dashboard prototype
- `HANUMA_Robotic_Mine_Safety (2).pdf` — presentation or report export
- `Patent Report.pdf` / `Patent Report.docx` — patent-related documentation
- `IDEA.pdf` / `IDEA.pptx` — concept and ideation materials
- `PNT Lab - Final Report ...docx` — formal internship and technical report source
- CSV data logs for telemetry and environmental analysis

## Use Case

HANUMA is intended to support:
- mine inspection and mapping
- hazardous gas detection
- low-light underground inspection
- rescue scouting before human entry
- autonomous telemetry gathering and reporting
- operator awareness in unsafe underground conditions

## Why This Project Matters

Traditional mine inspection relies heavily on manual human access, which is dangerous and inefficient. HANUMA addresses this by reducing risk through autonomous sensing, path planning, environment understanding, and communication resilience.

## GitHub Ready Push Commands

```bash
git init -b main
git add .
git commit -m "feat: initial HANUMA autonomous mine safety rover project upload"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/HANUMA_SIH2026.git
git push -u origin main
```

If prompted for credentials, use a GitHub Personal Access Token instead of the account password.

## Notes

- Keep Markdown documentation in GitHub for direct rendering.
- Keep presentations and compiled PDFs inside `docs/`.
- If model weights or large datasets are required, use Git LFS when necessary.
- Keep the repository public-facing and structured for evaluation and portfolio review.

## Project Summary

HANUMA represents a complete autonomous robotic platform for underground mine safety, combining embedded control, ROS 2 autonomy, sensor fusion, mapping, LiDAR perception, 3D vision, long-range communication, and actionable environmental monitoring in a single integrated system.
