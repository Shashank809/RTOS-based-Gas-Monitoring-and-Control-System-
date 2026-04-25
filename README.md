Gas Leak Emergency Shutdown & Ventilation Control System
Overview
This project implements a real-time gas leak detection and emergency response system using the ARM7 LPC2148 microcontroller.

It ensures safety by:
Detecting hazardous gas levels
Immediately shutting down motors
Activating ventilation
Sending alerts via UART

The system is designed for industrial and domestic safety applications.

Problem Statement

Design a system that:
Detects gas leakage
Stops all motors instantly
Activates exhaust ventilation
Triggers LED alerts
Sends UART notifications
Handles repeated gas spikes without missing events

Key Features
MQ-2 Gas Sensor (Digital Detection)
Emergency Motor Shutdown
Exhaust Fan Activation
LED Status Indication
UART Alert Messaging
RTOS-based Multitasking
Fast Real-Time Response (~75 ms)

System Architecture

As shown in the block diagram (page 4) :

Gas sensor feeds data to LPC2148
RTOS manages multiple tasks:
Gas Detection Task
Motor Control Task
Alarm Task
UART Communication Task
Outputs:
Motors OFF
Exhaust Fan ON
LED Alert
UART Message
