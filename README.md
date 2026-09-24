<h1 align="center">
  Electronic Differential (Torque Vectoring)
</h1>

<h4 align="center">
  A software-regulated torque distribution system for electric vehicles.
</h4>

<p align="center">
  <img src="https://img.shields.io/badge/MATLAB-0076A8?style=for-the-badge&logo=mathworks&logoColor=white"/>
  <img src="https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white"/>
  <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white"/>
  <img src="https://img.shields.io/badge/IoT_Cloud-333333?style=for-the-badge&logo=internet-of-things&logoColor=white"/>
</p>

---

## Overview
This project implements an Electronic Differential (E-Differential) system designed to replace conventional mechanical differentials in electric and hybrid vehicles. Instead of using physical gears to balance power, this system leverages real-time data processing and software algorithms to manage the speed of each wheel independently. 

## Key Features
* **Ackermann Steering Integration:** The system mathematically computes the required angular velocities for the inner and outer wheels during a turn using Ackermann's steering equations.
* **Dynamic Torque Vectoring:** Continuously monitors throttle input and steering angles to adjust power distribution instantly, preventing wheel slip and maintaining stability.
* **Real-Time IoT Telemetry:** Integrates with the Arduino IoT Cloud via an ESP8266 module to transmit live data on torque distribution, wheel speeds, and overall system health.
* **Fail-Safe Redundancy:** Includes fallback modes and redundant safety mechanisms to ensure vehicle stability in the event of hardware or sensor failure.

## System Architecture

The control loop is designed for rapid response to changing driving conditions:

1. **Sensor Input:** Wheel speed encoders, gyroscopes, and accelerometers provide continuous motion and traction data.
2. **Data Processing:** The central control unit uses Kalman filtering techniques to reduce sensor noise and ensure accurate measurements.
3. **Motor Control:** Independent software-controlled motors receive precise torque commands to adjust the left and right wheel speeds dynamically.

## Simulation & Validation
Before hardware implementation, the control logic was rigorously modeled and simulated using **MATLAB and Simulink**. The simulation analyzed transient response, energy efficiency, and stability across straight-line motion and cornering scenarios. 

## Performance Results
Hardware-in-the-loop testing and real-world prototype evaluations yielded the following validated improvements:
* **Energy Efficiency:** Achieved a 10-15% decrease in overall energy consumption, directly extending potential battery life.
* **Traction Control:** Demonstrated an average wheel slip reduction of 2.19% across various steering angles (5°, 15°, and 25°).
* **Torque Balance:** Maintained precise torque distribution balanced within a margin of $\pm3.4\%$.
