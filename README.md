# Project Sentinel – Flood Rescue Scout ROV

## Overview
Project Sentinel is a **semi-autonomous flood-response scout boat** designed to assist human rescue teams in hazardous flood-affected environments.  
The system operates as a **human-in-the-loop robotic platform**, where navigation is remotely controlled by an operator while onboard intelligence handles sensing and human detection.

The primary goal of this project is to **reduce risk to rescue personnel** by providing early visual reconnaissance, human detection, and location reporting before human entry into dangerous flood zones.

---

## Key Features
- 🚤 Remote-controlled surface vehicle (ROV)  
- 🧠 Edge AI-based human detection using onboard processing  
- 📷 Live video streaming for visual navigation  
- 📍 GPS-based location reporting upon detection  
- 📡 Obstacle detection using ultrasonic sensors  
- 🔋 Battery-powered system with solar-assisted charging  
- 👤 Human-in-the-loop control for safe navigation in debris-filled environments  

---

## System Architecture
Project Sentinel uses a **dual-processing architecture**:

### Raspberry Pi 5
- Handles camera input  
- Performs real-time human detection using computer vision  
- Runs all AI processing locally (no cloud dependency)  

### ESP32 DevKit V1
- Controls motors and propulsion  
- Interfaces with ultrasonic sensors and GPS module  
- Handles communication with the operator interface  

This separation ensures reliable low-level control while supporting computationally intensive perception tasks.

---

## Hardware Components
- Raspberry Pi 5  
- ESP32 DevKit V1  
- Camera Module (USB / CSI)  
- U-blox NEO-6M GPS Module  
- JSN-SR04T Waterproof Ultrasonic Sensor  
- L298N Motor Driver  
- 4 × DC Geared Motors  
- 3S Li-ion Battery Pack  
- Custom Floating Platform  

---

## Software Environment
- **Arduino IDE** – ESP32 firmware development  
- **Python** – Raspberry Pi system control and vision processing  
- **OpenCV / Computer Vision Libraries** – Human detection  
- **Serial / Wi-Fi Communication** – Inter-device and operator communication  

---

## Repository Structure
```text
project-sentinel-flood-rescue-rov/
│
├── esp32/                 # ESP32 motor control and sensor code
├── raspberry-pi/          # Camera, AI detection, and processing code
├── docs/                  # Block diagrams, figures, and report materials
├── README.md              # Project overview and documentation
