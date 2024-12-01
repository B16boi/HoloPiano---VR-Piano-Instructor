# HoloPiano: VR Piano Instructor
This is the project for Computer Science and Engineering Projects (II), NYCU.
Title: Real-Time Interactive VR System – Remote Piano Classroom 

## Authors
Syuan-Fu Hwang
Yu-Chun Lin
Ting-Yu Chou

## Features
- **Hand Tracking**: Accurate detection of hand positions and movements using Google MediaPipe.
- **Real-Time Visualization**: Displays and mirrors hand movements in a VR environment.
- **Interactive Piano Simulation**: Play virtual piano keys that react dynamically to hand movements.
- **Cross-Platform Integration**: Connects Android devices to VR through a custom server.
- **Hybrid TCP/UDP Server**: Asynchronous data streaming ensures a responsive experience.

## System Architecture
- **Server**: Listens for connections from the Recording client (Android app) and VR client (VR).
  - Implements a hybrid TCP/UDP protocol for efficient communication.
  - Relays hand data from Recording to VR clients asynchronously.
- **Recording Client (Android App)**: Captures hand movement using MediaPipe and streams data to the server.
- **VR Client (Unity3D)**: Receives hand data from the server and visualizes it in VR.
- **Visualization**: Hand data controls a virtual hand in the VR space, allowing interaction with piano keys.
  
## Server Workflow
1. Listens for connections on TCP (port `10001`) from both clients.
2. Assigns UDP ports dynamically to each client for data transfer.
3. Relays hand data from the Recording client to the VR client.

## Installation & Setup
```bash
# Repository Setup
git clone https://github.com/SFHSammay/HoloPiano---VR-Piano-Instructor.git
ˋˋˋ
