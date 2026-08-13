# Group μ - IoT Environmental Monitoring Dashboard

## 📊 Overview
Real-time IoT environmental monitoring system using:
- **ESP32** with DHT11, LDR, and Ultrasonic sensors
- **MQTT** (Mosquitto) for data transmission
- **Python Dash** for live dashboard visualization
- **Hardware feedback** via built-in LED

## 🔧 System Architecture
ESP32 Sensors → MQTT Broker → Python Server → Web Dashboard → LED Feedback

## 📦 Requirements
```bash
pip install -r requirements.txt
🚀 How to Run
1. Start MQTT Broker (Admin CMD)
   net start mosquito
2. Upload Arduino Code to ESP32
   Open esp32_mqtt_publisher.ino in Arduino IDE
   Change WiFi credentials and MQTT IP
   Upload to ESP32
3. Run Dashboard
   python dashboard.py
4. Open Browser
   http://127.0.0.1:8050
