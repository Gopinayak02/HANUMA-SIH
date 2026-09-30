# HANUMA Autonomous Mine Safety Rover

## Technical Project Report

## 1. Introduction

HANUMA is an autonomous robotic platform developed for underground mine inspection, hazard analysis, environmental surveillance, and emergency support in hazardous mining environments. The current design addresses a critical operational requirement: enabling safe observation and reconnaissance in spaces where human access is dangerous, unstable, or impractical.

The system combines mobile robotics, embedded hardware, sensing, communication, autonomy, and dashboard-based monitoring into a single integrated system intended for field deployment in complex underground conditions.

## 2. Problem Definition

Mining environments present multiple severe risks:
- poor visibility due to dust and smoke
- toxic gas exposure
- difficult navigation in narrow and uneven spaces
- reduced or absent GPS coverage
- poor communication reliability in metal-rich and obstructed environments
- potential structural instability and collapse risk

A mobile robotic system capable of sensing, navigating, and reporting these threats is highly valuable for operational safety and rescue support.

## 3. Objectives

The project was designed to achieve the following goals:

- build a rugged six-wheel mine rover platform
- integrate low-level control with embedded hardware
- implement high-level autonomy using ROS 2
- utilize LiDAR and perception sensors for obstacle avoidance
- fuse IMU and odometry for localization under GPS-denied conditions
- include SLAM and map-based navigation for underground operation
- monitor environmental parameters such as gas, dust, and humidity
- provide resilient communication with LoRa
- deliver real-time telemetry through a dashboard interface

## 4. Hardware Architecture

### 4.1 Chassis and Mobility
The rover platform uses a six-wheel rocker-bogie style chassis to improve traction and stability on uneven terrain. This mobility configuration enables controlled motion across disturbed surfaces and harsh operational conditions common in mining scenarios.

### 4.2 Embedded Control Layer
The low-level control system is implemented using ESP32, which handles:
- motor control
- sensor acquisition
- hardware safety checks
- embedded logic and fail-safe behavior

### 4.3 Computing Platform
The high-level intelligence is handled by a Raspberry Pi 5, which runs the ROS 2 software stack. This layer connects perception, navigation, localization, and communication modules into a working autonomous robot architecture.

## 5. Sensing and Perception

The system incorporates a multi-sensor perception stack to support environmental awareness and decision-making.

### 5.1 LiDAR
LiDAR offers robust obstacle detection and map building in constrained and low-visibility environments. It is a core component of the navigation and obstacle-avoidance strategy.

### 5.2 3D Vision
A 3D camera or depth-sensing module provides additional scene understanding and can help with object detection, terrain awareness, and real-time inspection in difficult visibility conditions.

### 5.3 Cameras and IR
Cameras provide visual feedback for inspection and navigation support. The inclusion of IR or low-light-capable vision improves situational awareness where dust, darkness, or smoke may limit standard optical visibility.

### 5.4 Environmental Sensors
The rover includes gas and air-quality sensing for parameters such as:
- CH4
- CO
- CO2
- O2
- H2S
- dust
- humidity
- temperature-related conditions

These measurements are essential for detecting mine hazards before humans enter unsafe areas.

## 6. Autonomous Navigation and Localization

The rover is designed for autonomous navigation in GPS-denied and partially unknown environments. The localization and navigation module is based on the combination of:
- wheel odometry
- IMU data
- LiDAR-based feature constraints
- map and obstacle awareness

This yields a robust navigation solution for corridor tracking, obstacle avoidance, and autonomous exploration in mine-like scenes.

## 7. SLAM and Mapping

A critical function of the system is map generation and environment understanding. The platform is designed to use a ROS 2-compatible SLAM workflow for:
- building an internal map of underground corridors
- estimating rover position within the environment
- identifying obstacles and constrained passages
- planning safe routes and return paths

This is particularly important in underground settings where GPS is unreliable or unavailable.

## 8. Communication System

Underground mining environments often experience signal attenuation and communication disruption. To address this challenge, HANUMA incorporates LoRa-based communication for resilient long-range telemetry.

This communication layer supports:
- remote health monitoring
- low-power long-range transmission
- telemetry streaming in constrained environments
- continuity of operation even when normal connectivity is weak

## 9. Dashboard and Telemetry

A custom dashboard provides real-time visibility of rover status and sensor information. The operator interface is designed to show:
- environmental conditions
- GPS or localization state
- gas sensor trends
- obstacle and map information
- rover health and motion status
- camera stream or remote visual feed

This improves situational awareness and reduces operator uncertainty during inspection missions.

## 10. Safety and Failsafe Logic

The rover design includes operational safety features such as:
- embedded watchdog logic
- fail-safe behavior for sensor anomalies
- communication-loss handling
- route-aware decision-making for risky conditions
- autonomous return or stabilization behavior in degraded scenarios

These mechanisms are important in mining operations where equipment reliability and safe behavior are essential.

## 11. Simulation and Validation

The platform was validated using simulation-based environments and system-level testing. The simulation framework was used to assess:
- terrain interaction
- obstacle handling
- navigation behavior
- sensor responsiveness
- dashboard telemetry workflow
- system readiness for mine-like conditions

This helps reduce risk before physical deployment and allows iterative improvement of the robot’s operational behavior.

## 12. Results and Discussion

The HANUMA prototype demonstrates the feasibility of an autonomous mine safety rover that can combine mobility, sensing, autonomy, and communication in one integrated platform. The implementation confirms the potential for:
- autonomous inspection in dangerous underground spaces
- gas and environmental hazard awareness
- remote monitoring and data logging
- improved safety through reduced human exposure

The system provides a practical foundation for real-world deployment in research, safety, and industrial mine-assistance scenarios.

## 13. Conclusion

HANUMA is a complete autonomous mine-safety robotic platform that integrates embedded control, ROS 2 autonomy, LiDAR and vision perception, localization, environmental monitoring, communication, and dashboard-based supervision. It addresses essential needs in underground mining operations, where safety, data collection, and autonomous navigation are critical.

The project demonstrates a strong interdisciplinary implementation of robotics, embedded systems, AI-enabled perception, and autonomous systems engineering for a high-risk real-world domain.

## 14. Final Project Presentation

This repository is intended to present the project in a professional and evaluable form, with documentation and assets arranged for GitHub visibility and technical review.
