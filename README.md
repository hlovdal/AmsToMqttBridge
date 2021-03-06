# AMS <-> MQTT Bridge

![](logo/powerlines.png?raw=true)
![](logo/simple_meter_icon.png?raw=true)
![](logo/bridge.png?raw=true)
![](logo/pcb.png?raw=true)
![](logo/network-transmit-receive.png?raw=true)

## Background
The purpose of this project is to collect information and build a simplified bridge for reading serial DLSM/M-bus information from electrical power meters (AMS), provided over the HAN port, and publishing to some IoT friendly target.

Components will be ESP8622, Arduino code, a (very simplified) M-bus <-> 3.3V serial interface

As a start, we should try to get information from the three types of AMS meters currently being installed in Norway. Some details about these are available here: [NVE_Info_kunder_HANgrensesnitt.pdf](Documentation/NVE_Info_kunder_HANgrensesnitt.pdf)

The project should include:
- [x] [Simple circuit to transform MBus levels to 3.3V serial](/Electrical/HAN_ESP_Simple)
- [x] [Code to capture and analyze data from PC](/Code/HanDebugger)
- [x] [Code to capture and analyze data from Arduino](/Code/ESPDebugger)
- [x] [Sample data from various meters](/Samples)
- [x] [Documentation on HAN / MBus / DLMS/COSEM](/Documentation)
- [X] [Code to parse DLMS data into a structure](/Code/Arduino/HanReader/src)
- [X] [Real schematics, including ESP8266](/Electrical/HAN_ESP_Simple/PCB)
- [X] [PCB layout](/Electrical/HAN_ESP_Simple/PCB)
- [ ] Arduino library
- [X] [Arduino sample sketch to read values and report to MQTT server](/Code/Arduino)

## Electrical design

One original hardware design has been made and a new one is currently being developed.
More details in [electrical design](./Electrical).


### Circuit prototype
![Breadboard](Electrical/HAN_ESP_Simple/Prototype.jpg)

### MQTT output
![MQTT screenshot](Electrical/HAN_ESP_Simple/MQTT%20screenshot.png)
