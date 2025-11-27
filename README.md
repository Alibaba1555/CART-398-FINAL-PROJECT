# Info Smog — Learning to See Movement  
### An interactive information-fog visualization driven by depth features and machine learning.

## Overview
**Info Smog** visualizes digital information overload as a living fog that reacts to the viewer’s body.  
Using a depth camera and a lightweight machine-learning model, the system interprets proximity, movement stability, motion intensity, and screen occupancy, transforming these signals into the behavior of a swirling cloud of text.

The closer you move, the more chaotic the fog becomes.  
The more violently you move, the faster it storms.  
The more you block the screen, the thicker and more overwhelming the fog grows.

## Concept
In our original proposal, *Learning to See Movement*, the goal was to teach a system to interpret human motion through depth.  
Info Smog extends this idea by assigning meaning to those movements:  
your gestures become disturbances inside a dense cloud of notifications, ads, and algorithmic noise.

## System Overview
The project operates through a simple pipeline:

1. **Depth Camera**  
   Captures only distance and motion — not color or facial features.

2. **Depth Features Extraction**  
   - Mean depth (proximity)  
   - Depth variance (movement stability)  
   - Delta depth (motion speed)  
   - Occupancy rate (screen coverage)

3. **Wekinator (ML Mapping)**  
   Learns how these features should influence the fog's behavior.

4. **Processing Visualization**  
   Turns the learned rules into motion:  
   text density, speed, jitter, expansion, and visual “overload.”

## Interaction
- **Move closer** → denser, brighter, more overwhelming fog  
- **Move steadily** → calm behavior  
- **Move violently** → jittery, storm-like motion  
- **Cover the camera** → fog saturates the screen  

## Technologies Used
- **Processing (P2D)**  
- **Wekinator (Regression model)**  
- **Depth Camera** (Intel RealSense / Kinect-style)  
- **OSC Communication**

## Running the Project
1. Start your depth-camera python file (mean depth, variance, etc.).  
2. Launch Wekinator and load the provided model preset.  
3. Start the Processing sketch (`particles.pde`).  
4. Ensure OSC ports match between Wekinator and Processing.  
5. Move in front of the camera and interact with the fog.

## Credits
Created by **[Tianshun Wu and Junming He]**  
CART 398 — Creative Machine Learning  
Concordia University, 2025  
