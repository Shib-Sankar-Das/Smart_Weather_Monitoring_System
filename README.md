# Smart Weather Monitoring System 🌤️

A real-time weather monitoring system using the ESP8266, the New Blynk app, DHT11 for temperature and humidity, BMP180 for atmospheric pressure, a rain sensor, and an LDR for light detection. This project displays weather data on an LCD and sends it to the Blynk app for remote monitoring.

## Introduction 📖

This Weather Monitoring System allows users to monitor weather conditions such as temperature, humidity, pressure, rain, and light levels remotely via the Blynk IoT platform. Using various sensors and the Blynk app, you can keep track of real-time weather changes, enhancing the system's utility for smart agriculture, environmental monitoring, and IoT applications.

## Approach 💡

1. **Sensor Integration**: We use DHT11, BMP180, rain, and LDR sensors for capturing weather data.
2. **Data Processing**: The ESP8266 processes and uploads the data to the Blynk cloud.
3. **LCD Display**: A 16x2 I2C LCD shows real-time weather data locally.
4. **Blynk App**: The Blynk IoT platform provides a dashboard to remotely monitor data and set notifications.

## Usability 🛠️

- **Agriculture**: Monitors weather conditions for optimal farming conditions.
- **Smart Home**: Can be integrated into home automation systems for weather-based actions.
- **Environmental Monitoring**: Tracks environmental changes in real-time for research or safety measures.
- **Educational Tool**: A great project for students to learn IoT and embedded systems.

## Project Impact 🌍

This project offers an accessible way to monitor weather remotely, supporting applications in agriculture, smart homes, and environmental research. Its real-time data processing enhances decision-making and helps conserve resources by monitoring weather patterns effectively.

## Hardware Components 🧩

- ESP8266 Wi-Fi Module
- DHT11 Temperature & Humidity Sensor
- BMP180 Atmospheric Pressure Sensor
- Rain Sensor
- LDR (Light Dependent Resistor)
- 16x2 I2C LCD Display
- Connecting Wires

## Circuit Diagram 📷

![Circuit-3-removebg-preview](https://github.com/user-attachments/assets/9eb235a2-c0e1-4b8f-9865-0a08a92cdc74)


## Circuit Pin Connections 📝

| Component         | Pin on ESP8266 |
|-------------------|----------------|
| DHT11             | GPIO 2         |
| BMP180            | SDA (D1), SCL (D2) |
| Rain Sensor       | A0             |
| LDR               | GPIO 16        |
| LCD SDA           | D1             |
| LCD SCL           | D2             |

## Blynk Virtual Pins 📲

| Parameter          | Blynk Virtual Pin |
|--------------------|-------------------|
| Temperature        | V0                |
| Humidity           | V1                |
| Rain               | V2                |
| Pressure           | V3                |
| Light (LED status) | V4                |

## Installation & Setup ⚙️

1. **Blynk Configuration**:
   - Download the [Blynk app](https://blynk.io/) and create a new project.
   - Configure the Blynk template ID, device name, and authentication token in the code.

2. **Code Setup**:
   - Install necessary libraries: `DHT`, `LiquidCrystal_I2C`, `BlynkSimpleEsp8266`, and `SFE_BMP180`.
   - Copy and paste the code into the Arduino IDE.
   - Update Wi-Fi credentials and Blynk auth token in the code.
   - Upload the code to ESP8266 using the Arduino IDE.

3. **Run the System**:
   - Power up the ESP8266, and the LCD will display weather data.
   - Open the Blynk app to view real-time weather data.

## Demo Video 📹

**(Embed or link to a demo video showcasing the project)**

## Code Structure 🖥️

The main functions include:

- `DHT11sensor()`: Reads temperature and humidity.
- `rainSensor()`: Reads rain sensor data.
- `pressure()`: Captures pressure data from the BMP180.
- `LDRsensor()`: Checks light levels and updates Blynk LED widget.

