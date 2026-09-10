# 🚰 Smart Submersible Pump Controller (ESPHome)

[![ESPHome](https://img.shields.io/badge/ESPHome-2025.12.7-orange?style=for-the-badge&logo=esphome)](https://esphome.io)
[![Home Assistant](https://img.shields.io/badge/Home_Assistant-Compatible-blue?style=for-the-badge&logo=home-assistant)](https://home-assistant.io)
[![GitHub Star](https://img.shields.io/github/stars/ElectroIoT/Smart-Submersible-Pump-Controller-ESPHome?style=for-the-badge)](https://github.com/ElectroIoT/Smart-Submersible-Pump-Controller-ESPHome/stargazers)

An advanced IoT solution for single-phase submersible pumps. This project replaces or augments your manual motor starter with a smart, WiFi-enabled controller featuring **Dry-Run Protection**, **Energy Monitoring**, and **Real-time Feedback**.

---

## 📸 Project Showcase

### Hardware Build
<p align="center">
  <img src="Image/controler.jpeg" width="45%" alt="Controller Front View" />
  <img src="Image/controler2.jpeg" width="45%" alt="Controller Side View" />
</p>

### Home Assistant Dashboard
<p align="center">
  <img src="Image/motor_1.png" width="45%" alt="Dashboard Idle" />
  <img src="Image/motor_started.png" width="45%" alt="Dashboard Active" />
</p>

---

## 📺 Video Demo
Experience the smart controller in action. See the real-time feedback and relay switching.

<p align="center">
  <video src="demo.mp4" width="100%" controls>
    Your browser does not support the video tag.
  </video>
</p>

---

## ✨ Key Features

- **Dual-Phase Control:** Precise 2-second pulses for Start and Stop relays.
- **Dry-Run Protection:** Automatically shuts down the motor if current (Amps) drops below a safe threshold.
- **Power Monitoring:** Real-time Voltage, Current (Amps), Watts, and Total Energy (kWh) tracking via PZEM-004T.
- **Dual SSID Support:** Automatically switches between primary and secondary WiFi networks.
- **Industrial Dashboard:** Attractive, high-visibility Home Assistant UI with dynamic color-coded buttons.

---

## 🛠 Hardware Required

| Component | Purpose |
| :--- | :--- |
| **Wemos D1 Mini** | The Brain (ESP8266) |
| **PZEM-004T V3.0** | AC Energy Monitoring & Protection |
| **2-Channel Relay** | High-Voltage Switching (Start/Stop) |
| **Hi-Link HLK-PM01** | 5V DC Isolated Power Supply |

---

## 📐 Wiring Guide

### Pin Mapping:
- **Relay 1 (Start):** GPIO5 (D1)
- **Relay 2 (Stop):** GPIO4 (D2)
- **PZEM RX:** GPIO14 (D5)
- **PZEM TX:** GPIO12 (D6)

---

## 🤝 Credits & Contributions

This project was made possible with contributions and technical guidance from:

- **Lead Developer:** [Your Name/Blog Name]
- **Technical Contributor:** [@manoranjan2050](https://github.com/manoranjan2050)

---

## ⚠️ Safety Disclaimer

> **DANGER: HIGH VOLTAGE.** This project involves 230V AC wiring. Improper installation can lead to electrical shock, fire, or damage to your motor. Always disconnect the main breaker before working on the panel.

## 📝 License
Licensed under the MIT License.