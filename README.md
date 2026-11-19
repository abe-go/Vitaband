
# VitaBand
### Wearable Health Monitoring and Emergency Alert System

## Overview

VitaBand is an ESP32-based wearable monitoring and emergency alert system designed to provide remote monitoring of a user's health-related readings, physical activity, and location.

The system integrates multiple sensors to collect information such as heart rate, movement, and GPS coordinates. Through LoRa wireless communication, the wearable device transmits collected data to a separate base station, allowing monitoring personnel to receive updates and respond to emergency situations.

VitaBand also features an SOS button that allows the wearer to send an emergency alert. Once the base station receives the alert, monitoring personnel can acknowledge the request, sending a confirmation signal back to the wearable device. A vibration motor provides haptic feedback to notify the wearer that the alert has been acknowledged.

The project aims to demonstrate how wearable technology and long-range wireless communication can support remote monitoring and emergency response.

## Objectives

- Develop a wearable monitoring device using ESP32.
- Monitor heart rate and physical activity.
- Track the user's location through GPS.
- Transmit monitoring data wirelessly using LoRa.
- Provide an emergency SOS alert mechanism.
- Establish two-way communication between the wearable and base station.
- Provide haptic feedback when an emergency alert is acknowledged.

## Main Components

### Wearable Device
- ESP32 Microcontroller
- MAX30102 Heart Rate Sensor
- ADXL345 Accelerometer
- NEO-6M GPS Module
- SX1278 Ra-02 LoRa Module (433 MHz)
- 1.3-inch OLED Display (SH1106)
- SOS Push Button
- Vibration Motor (MLE00901)
- Motor Driver Circuit

### Base Station
- ESP32 Microcontroller
- SX1278 Ra-02 LoRa Module
- Display / Monitoring Interface
- Alarm or Buzzer
- Acknowledgment Push Button

## Technologies Used

- Arduino IDE
- Embedded C++
- ESP32
- LoRa Wireless Communication
- GPS Tracking
- Sensor Integration
- I2C Communication
- SPI Communication
- UART Communication

## Key Features

### 1. Heart Rate Monitoring
Uses the MAX30102 sensor to collect heart-rate readings and detect finger contact.

### 2. Movement Monitoring
Uses the ADXL345 accelerometer to monitor the wearer's movement and physical activity.

### 3. GPS Location Tracking
Uses the NEO-6M GPS module to obtain the wearer's geographical coordinates.

### 4. Long-Range Wireless Communication
Uses the SX1278 LoRa module to transmit sensor readings, activity information, and GPS coordinates to the base station.

### 5. Emergency SOS Alert
Includes a dedicated SOS button that allows the wearer to send an emergency notification to the monitoring station.

### 6. Two-Way Communication
Allows the base station to acknowledge received SOS alerts and send confirmation messages back to the wearable device.

### 7. Haptic Feedback
Uses a vibration motor to notify the wearer when an emergency acknowledgment is received.

### 8. OLED Display
Displays relevant monitoring information and device status directly on the wearable.

## System Operation

1. The wearable device initializes its sensors and communication modules.
2. The MAX30102 collects heart-rate readings when finger contact is detected.
3. The ADXL345 monitors the wearer's movement.
4. The NEO-6M GPS obtains location coordinates when a GPS fix is available.
5. The ESP32 processes the collected information.
6. Sensor readings and location data are transmitted to the base station through LoRa.
7. The wearer can press the SOS button to send an emergency alert.
8. The base station receives and displays the alert.
9. Monitoring personnel acknowledge the emergency notification.
10. The wearable receives the acknowledgment and activates its vibration motor.


## Development Status

Prototype development and hardware integration. Individual sensor testing, ESP32 programming, LoRa communication, and wearable-to-base-station data transmission have been explored.

Further integration and testing are needed to establish reliable operation of all sensors, GPS reception, emergency alerts, and acknowledgment functions.

## Applications

- Remote personnel monitoring
- Field operation safety
- Emergency notification systems
- Wearable IoT applications
- Remote health-related monitoring

## Limitations

- Heart-rate readings depend on proper sensor contact and signal quality.
- GPS accuracy depends on satellite reception and environmental conditions.
- LoRa communication depends on distance, antenna configuration, and surrounding interference.
- The prototype is not a certified medical device and is not intended for clinical diagnosis.

## Future Improvements

- Develop a dedicated real-time base station dashboard.
- Improve sensor reading stability.
- Enhance GPS and LoRa communication reliability.
- Integrate historical monitoring records.
- Improve wearable enclosure and battery management.

