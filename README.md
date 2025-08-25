# WaterMeter_Sensor_Zigbee
A solar powered esp32-c6 based sensor that monitors pulses on the Itron TD8 water meter and transmits these via Zigbee.

I have an Itron TD8 water meter at home in Australia, with a spinning metal disk thing that goes around once per 0.01m^3 water consumption. To integrate this into HomeAssistant, I was inspired by similar projects using inductive proximity sensors to meter these spinning pulses. However - I wanted a neat and self-contained zigbee and solar-powered solution rather than wired WiFi projects already available. So I made my own using the DFRobot Firebeetle esp32-c6 as a platform.

# Hardware
Required components:
-- DFRobot FireBeetle 2 ESP32-C6
-- LJ 5v proximity sensor
-- DC-DC Boost Converter Module
-- 3.3v-5v Logic Level Shifter
-- 3x18650 batteries
-- 5v solar panel
-- Waterproof housing
-- Perfboard
-- Wires etc

# Software
