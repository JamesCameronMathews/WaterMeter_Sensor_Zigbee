# WaterMeter_Sensor_Zigbee
A solar powered esp32-c6 based sensor that monitors pulses on the Itron TD8 water meter and transmits these via Zigbee.

I have an Itron TD8 water meter at home in Australia, with a spinning metal disk thing that goes around once per 0.01m^3 water consumption. To integrate this into HomeAssistant, I was inspired by similar projects using inductive proximity sensors to meter these spinning pulses. However - I wanted a neat and self-contained zigbee and solar-powered solution rather than wired WiFi projects already available. So I made my own using the DFRobot Firebeetle esp32-c6 as a platform.


