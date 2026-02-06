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

project-sentinel-flood-rescue-rov/
│
├── esp32/                 # ESP32 motor control and sensor code
├── raspberry-pi/          # Camera, AI detection, and processing code
├── docs/                  # Block diagrams, figures, and report materials
├── README.md              # Project overview and documentation

## How the System Works
1. The operator remotely controls the boat using a laptop or mobile device.  
2. The onboard camera streams live video from the boat to the operator.  
3. The Raspberry Pi processes video frames in real time to detect humans.  
4. When a human is detected:
   - An alert is generated  
   - GPS coordinates are collected  
   - Location data is transmitted to the operator  
5. Ultrasonic sensors continuously monitor obstacles and assist safe navigation.

---

## Testing and Validation
The prototype was tested in a **controlled water environment**, where it:
- Successfully floated and maneuvered on water  
- Streamed live video reliably  
- Detected human presence in real time  
- Reported GPS coordinates upon detection  
- Responded correctly to remote control commands  

---

## Project Status
- ✔ Prototype implemented  
- ✔ Hardware tested on water  
- ✔ Human detection validated  
- ✔ Results documented in project report  

---

## Authors
This project was developed as part of an academic project by students of the  
**Department of Computer Science and Engineering, United International University, Dhaka, Bangladesh**.

---

## License
This project is intended for **academic and research purposes**.
