# Gas Leak Emergency Shutdown & Ventilation Control System

## Overview
This project implements a real-time gas leak detection and emergency response system using the ARM7 LPC2148 microcontroller.

The system ensures safety by:
- Detecting hazardous gas levels
- Immediately shutting down motors
- Activating ventilation
- Sending alerts via UART

It is designed for industrial and domestic safety applications.

---

## Problem Statement
Design a system that:
- Detects gas leakage
- Stops all motors instantly
- Activates exhaust ventilation
- Triggers LED alerts
- Sends UART notifications
- Handles repeated gas spikes without missing events

---

## Key Features
- MQ-2 Gas Sensor (Digital Detection)
- Emergency Motor Shutdown
- Exhaust Fan Activation
- LED Status Indication
- UART Alert Messaging
- RTOS-based Multitasking
- Fast Real-Time Response (~75 ms)

---

## System Architecture
The system consists of:
- Gas Sensor connected to LPC2148
- RTOS managing multiple tasks:
  - Gas Detection Task
  - Motor Control Task
  - Alarm Task
  - UART Communication Task

Outputs:
- Motors OFF
- Exhaust Fan ON
- LED Alert
- UART Message

---

## Hardware Components

| Component        | Description                     | LPC2148 Pin       |
|------------------|---------------------------------|------------------|
| MQ-2 Gas Sensor  | Detects LPG, CO, Smoke         | P0.3             |
| DC Motor         | Emergency control              | P0.8, P0.11      |
| L293D Driver     | Motor driver                   | P0.8, P0.11      |
| Stepper Motor    | Normal operation               | P0.12–P0.15      |
| ULN2003 Driver   | Stepper driver                 | P0.12–P0.15      |
| LED Indicator    | Status display                 | P0.7             |
| UART0            | Communication                 | P0.0, P0.1       |

---

## Interfacing
- MQ-2 sensor connected to digital input
- Motors controlled using L293D and ULN2003 drivers
- UART connected to terminal for alerts

---

## Performance Analysis

### Time Analysis
- Gas Detection Task: 50 ms
- Control Task: 10 ms
- UART Execution: 15 ms

Total Response Time ≈ 75 ms

### Memory Usage
- FLASH: 4.26 KB
- RAM: 4.29 KB

---

## Simulation and Results
- Simulated using Keil uVision4
- Hardware implementation verified
- Circuit emulation tested

Observed Results:
- Immediate motor shutdown on gas detection
- Ventilation activated successfully
- LED and UART alerts triggered reliably

---

## Software Design
- Embedded C
- RTOS-based task scheduling
- UART communication (9600 baud, 8N1)


---

## Applications
- Industrial safety systems
- Smart homes
- Gas storage facilities
- Laboratories

---

## Conclusion
The system provides a reliable real-time safety solution using RTOS-based multitasking. It effectively handles repeated gas leakage events and ensures fast emergency response, making it suitable for safety-critical environments.

---
