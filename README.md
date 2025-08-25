
# 💧 WaterMeter_Sensor_Zigbee

A **solar-powered ESP32-C6-based sensor** that monitors pulses on the **Itron TD8 water meter** and transmits data via **Zigbee**, designed for integration with **Home Assistant**.

## Project Overview

I have an **Itron TD8 water meter** at home in Australia, which features a **spinning metal disk** that completes one rotation per **0.01 m³** of water consumption. Inspired by similar DIY projects using **inductive proximity sensors**, I wanted a **self-contained**, **solar-powered**, and **Zigbee-compatible** solution—rather than relying on wired Wi-Fi setups.

So I built my own using the **DFRobot FireBeetle ESP32-C6** platform.

![Itron TD8 Water Meter](https://5.imimg.com/data5/ANDROID/Default/2022/6/LH/GU/CT/16071330/product-jpeg-500x500.jpg)

---

## 🔧 Hardware Components

| Component | Description |
|----------|-------------|
| [DFRobot FireBeetle 2 ESP32-C6](https://www.dfrobot.com/product-2830.html) | Low-power ESP32-C6 board with Zigbee support |
| LJ 5V Proximity Sensor | Detects the spinning metal disk pulses |
| DC-DC Boost Converter Module | Boosts voltage from battery to 5V for sensor |
| 3.3V–5V Logic Level Shifter | Ensures compatibility between sensor and ESP32 |
| 3x 18650 Lithium Batteries | Power storage for solar charging |
| 5V Solar Panel | Charges the batteries during daylight |
| Waterproof Housing | Protects electronics from weather |
| Perfboard & Wires | For mounting and connections |

---

## 💻 Software Implementation

- Developed using **Arduino IDE** with **Espressif Zigbee** and **PCNT (Pulse Counter)** libraries.
- The sensor is registered as a **simple analog Zigbee sensor**.
- Reports:
  - **Pulse count** (water usage)
  - **Battery percentage**
- **Sleep logic** is not fully implemented yet, as it interferes with PCNT functionality.

---

## 🏡 Home Assistant Integration

Once paired via Zigbee, the sensor appears as a battery-powered analog device. You can use the pulse count to calculate water usage and set up automations or alerts in Home Assistant.

---

## 📌 Future Improvements

- Implement deep sleep logic without disrupting PCNT.
- Add enclosure temperature/humidity/air pressure monitoring.
- Optimize solar charging and battery management.
