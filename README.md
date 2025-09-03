🚗 Automotive CAN-to-WiFi Converter(PCB DESIGN)
📌 Overview

This project implements an Automotive CAN (Controller Area Network) to Wi-Fi converter using a microcontroller with integrated Wi-Fi and a custom PCB designed in KiCad.
It allows vehicles’ CAN bus data (speed, RPM, fuel level, sensor data, etc.) to be captured, processed, and transmitted over Wi-Fi to mobile apps.

🚀 Features

Interfaces with standard Automotive CAN bus (OBD-II, ISO 11898)

Converts CAN frames into Wi-Fi packets

Supports protocols: MQTT, HTTP, WebSocket

Designed for low-latency data streaming

Custom KiCad PCB with CAN transceiver + Wi-Fi MCU

Optional SD card logging for offline analysis

Can be used for telematics, diagnostics, and fleet monitoring

🛠️ Hardware Components

Microcontroller (ESP32 / STM32 + ESP8266) → Wi-Fi + processing

CAN Transceiver (MCP2551 / SN65HVD230) → Interface between CAN bus & MCU

OBD-II Connector → Connection to vehicle CAN lines (CAN_H, CAN_L)

Power Supply

12V from car → Buck converter → 5V/3.3V regulated

Automotive-grade regulator (LM2596 / MP1584)

Protection Circuits

TVS Diodes for CAN line protection

Fuse & reverse polarity protection

Optional Modules

SD card (logging)

OLED/LCD (local display)

📐 PCB Design (KiCad)

Designed using KiCad EDA

2-layer PCB optimized for automotive use

Includes CAN transceiver + ESP32 footprint

Proper decoupling capacitors and EMI filters

Ground plane isolation between noisy CAN and Wi-Fi section

Connector footprint for OBD-II interface

Gerber files ready for fabrication

⚙️ Firmware / Software

Developed using Arduino IDE / ESP-IDF / STM32Cube

Features:

Reads CAN frames via CAN transceiver

Publishes data over Wi-Fi (MQTT/HTTP/WebSocket)

Supports real-time monitoring dashboard

Configurable baud rates (125 kbps, 250 kbps, 500 kbps)

🧩 Applications

Vehicle diagnostics (OBD-II data monitoring)

Fleet management & telematics

Real-time performance tracking (RPM, speed, fuel, etc.)

Research & development for automotive IoT

Data logging for predictive maintenance

⚠️ Safety Note

⚡ Caution: This project connects directly to the vehicle’s CAN bus. Incorrect wiring may damage ECU or other vehicle electronics. Ensure proper isolation and automotive-grade components are used.

📖 Future Enhancements

Support for Bluetooth + Wi-Fi dual mode

Cloud analytics with AI for predictive maintenance

Encryption for secure vehicle data transfer

Integration with mobile OBD-II diagnostic apps

