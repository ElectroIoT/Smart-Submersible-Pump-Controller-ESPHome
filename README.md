# 🚰 Smart Submersible Pump Controller (ESPHome)

[![ESPHome](https://img.shields.io/badge/ESPHome-2025.12.7-orange?style=for-the-badge&logo=esphome)](https://esphome.io)
[![Home Assistant](https://img.shields.io/badge/Home_Assistant-Compatible-blue?style=for-the-badge&logo=home-assistant)](https://home-assistant.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

An advanced IoT solution for single-phase submersible pumps. This project replaces or augments your manual motor starter with a smart, WiFi-enabled controller featuring **Dry-Run Protection**, **Energy Monitoring**, and **Real-time Feedback**.

---

## ✨ Features

- **Dual-Phase Control:** Precise 2-second pulses for Start and Stop relays.
- **Dry-Run Protection:** Automatically shuts down the motor if current (Amps) drops below a safe threshold.
- **Power Monitoring:** Real-time Voltage, Current (Amps), Watts, and Total Energy (kWh) tracking via PZEM-004T.
- **Dual SSID Support:** Automatically switches between primary and secondary WiFi networks.
- **Static IP:** Stable connection with manual IP configuration.
- **Industrial Dashboard:** Attractive, high-visibility Home Assistant UI with dynamic color-coded buttons.

---

## 🛠 Hardware Required

| Component | Purpose |
| :--- | :--- |
| **Wemos D1 Mini** | The Brain (ESP8266) |
| **PZEM-004T V3.0** | AC Energy Monitoring & Protection |
| **2-Channel Relay** | High-Voltage Switching (Start/Stop) |
| **Hi-Link HLK-PM01** | 5V DC Isolated Power Supply |
| **CT Coil** | Current Sensing (Included with PZEM) |

---

## 📐 Wiring Diagram

[Image of Wemos D1 Mini connected to a 2-channel relay and PZEM-004T for pump control]

### Pin Mapping:
- **Relay 1 (Start):** GPIO5 (D1)
- **Relay 2 (Stop):** GPIO4 (D2)
- **PZEM RX:** GPIO14 (D5)
- **PZEM TX:** GPIO12 (D6)

---

## 🚀 Installation

### 1. ESPHome Setup
Choose your version from the repository:
- **`basic_controller.yaml`:** Relay control only.
- **`pro_controller.yaml`:** Full power monitoring + Dry-run protection.

### 2. Configuration
Before flashing, ensure you update the following in the YAML files:
- WiFi SSIDs and Passwords
- ESPHome API Encryption Key
- Static IP details (Gateway/Subnet)

### 3. Flash the Device
```bash
esphome run your_config_file.yaml# Smart-Submersible-Pump-Controller-ESPHome
