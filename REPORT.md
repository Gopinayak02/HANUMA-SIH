# HANUMA Autonomous Mine Safety Rover

## Project Report

## 1. Introduction

HANUMA is an autonomous robotic platform designed for underground mine safety, inspection, and emergency support in hazardous environments. The project focuses on developing a rover that can navigate rough terrain, detect hazards, monitor environmental conditions, and provide remote situational awareness in GPS-denied and low-visibility mine corridors.

The rover combines embedded control, ROS 2 autonomy, sensor fusion, perception, communication, and remote dashboarding into one integrated system. The design ensures an effective approach for mine safety applications where human entry may be dangerous or impossible.

## 2. Problem Context

Underground mining environments present severe challenges including:
- poor visibility from dust and smoke
- hazardous gases such as methane, carbon monoxide, and oxygen deficiency
- narrow and unpredictable terrain
- limited GPS and communication coverage
- risk of structural instability and collapse

Human inspection in such environments is highly risky. HANUMA addresses this by enabling autonomous reconnaissance, environmental monitoring, and hazard detection before humans enter the area.

## 3. Objectives

The main objectives of the project were to:

- develop a robust six-wheel rover platform for rough terrain
- integrate embedded and high-level computing architecture
- implement ROS 2-based autonomy and navigation
- use LiDAR and depth/vision sensing for perception and obstacle avoidance
- incorporate IMU and odometry for localization in GPS-denied conditions
- deploy SLAM and path planning for autonomous exploration
- monitor gas, dust, temperature, and environmental safety parameters
- establish resilient communication using LoRa for low-connectivity environments
- provide real-time telemetry and a remote monitoring dashboard

## 4. System Architecture

### 4.1 Embedded Layer
The lower-level control layer is based on ESP32 hardware, which handles:
- motor control and PWM signals
- sensor acquisition
- watchdog and fail-safe logic
- data handling between sensors and processing units

### 4.2 High-Level Intelligence Layer
The high-level embedded intelligence is handled by a Raspberry Pi 5 running ROS 2. This layer is responsible for:
- sensor drivers
- navigation and planning
- localization and mapping
- communication with the dashboard
- perception and AI-based detection

### 4.3 Perception Modules
The perception stack includes:
- 2D LiDAR for obstacle detection and feature mapping
- 3D camera / depth sensor for scene understanding and object detection
- HD or IR camera for visibility under low light
- IMU for motion and orientation estimation
- Wheel odometry for relative movement estimation

### 4.4 Environmental Monitoring
The rover additionally monitors:
- CH4
- CO
- CO2
- O2
- H2S
- dust
- humidity
- temperature and vibration-related parameters

These measurements are critical for identifying dangerous conditions before or during entry into mine areas.

## 5. Autonomous Navigation and Localization

HANUMA is designed for localization and navigation in environments where GPS signals are unreliable or unavailable. The system uses a fused perception approach combining:

- wheel odometry
- IMU data
- LiDAR observations
- map-based localization constraints

The rover uses ROS 2 navigation tools to generate paths, estimate cost maps, and avoid obstacles while navigating underground corridors. This makes the platform useful for autonomous inspection and rescue support missions.

## 6. SLAM and Mapping

The platform is intended to operate with a ROS 2 SLAM and mapping pipeline for creating and maintaining a map of the mine environment. This is especially beneficial for:
- corridor exploration
- understanding environmental topology
- planning return routes
- locating hazardous zones
- map-based autonomous navigation

The design is suited for GPS-denied indoor and underground navigation conditions.

## 7. Communication System

Mine environments are often characterized by severe RF attenuation and difficult communication conditions. HANUMA includes LoRa-based communication concepts to support resilient telemetry and control communication over longer distances and through obstructive environments.

The communication approach supports:
- remote telemetry
- low-power long-range reporting
- operator awareness during remote operations
- fallback and failsafe behavior when connectivity weakens

## 8. Dashboard and Remote Monitoring

A real-time telemetry dashboard was developed to present:
- rover position and status
- gas trends
- environmental data
- obstacle information
- navigation state
- live stream or camera feed
- system health indicators

This interface enables remote supervision and supports mission planning and rapid hazard response.

## 9. Control and Safety Logic

The system was designed with safety in mind, including:
- low-level hardware watchdog logic
- failsafe conditions for communication drop or sensor abnormalities
- route-aware navigation behavior
- restricted motion in risky conditions
- autonomous return-to-communication logic in degraded states

These features improve operational reliability in dangerous conditions.

## 10. Methodology

The system was developed in stages:

1. requirement analysis for underground mine safety
2. mechanical platform design and rocker-bogie chassis formulation
3. embedded hardware integration for sensors and motors
4. Raspberry Pi 5 setup with ROS 2 and driver integration
5. LiDAR, IMU, odometry, and vision sensor calibration
6. localization and mapping workflow development
7. ROS 2 navigation and path planning implementation
8. environmental monitoring and hazard detection integration
9. LoRa communication and dashboard integration
10. validation in simulated or field-like environments

## 11. Simulation and Validation

Validation was performed through simulation, sensor-driven testing, and prototype demonstration. The platform was evaluated for:
- mobility on uneven terrain
- navigation through constrained spaces
- sensor response in rough environments
- dashboard data integrity
- communication reliability
- hazard monitoring effectiveness

The simulation environment helps evaluate mine-like conditions before actual deployment in the field.

## 12. Results and Discussion

The prototype demonstrates the feasibility of an autonomous rover for underground mine monitoring and inspection. The integrated platform successfully combines:
- mechanical mobility
- ROS 2 autonomy
- mapping and navigation
- environmental sensing
- low-level embedded control
- remote monitoring

This confirms the practicality of a mine-focused autonomous robotic system for safety and reconnaissance operations.

## 13. Project Significance

HANUMA is relevant to modern mining safety because it reduces dependence on direct human exposure in dangerous zones. The project demonstrates a practical application of robotics, embedded systems, autonomy, perception, communication, and remote monitoring for operational mine safety.

## 14. Conclusion

HANUMA is a compact, autonomous, and mission-oriented rover built specifically for underground mine hazard analysis and navigation support. Through the integration of ROS 2, SLAM, LiDAR, 3D vision, environmental sensing, embedded control, and LoRa communication, the system addresses multiple challenges of mine inspection and rescue support.

The project represents a strong interdisciplinary implementation of robotics engineering, autonomous systems, and safety-focused industrial application.

## 15. Recommended GitHub Presentation Layout

For public portfolio and evaluation use, the repository should present:
- `README.md` — overview and architecture
- `REPORT.md` — technical project report
- `docs/` — presentations, PDFs, diagrams, images
- `firmware/` — embedded code and driver logic
- `ros2_ws/` — ROS 2 packages and launch files
- `dashboard/` — monitoring interface
- `edge_ai/` — vision and detection scripts
- `simulation/` — Gazebo/Webots validation assets

This structure provides a clear and professional presentation of the project for GitHub reviewers, evaluators, and collaborators.
