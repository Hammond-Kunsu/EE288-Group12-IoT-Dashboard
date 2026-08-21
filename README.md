# IoT Environmental Monitoring Dashboard

A real-time environmental monitoring system built with an ESP32, MQTT, and Python Dash. The system reads sensor data from an ESP32, publishes it through an MQTT broker, and displays live measurements, alerts, and trends in a browser dashboard.

> Developed for the Electrical Measurement and Instrumentation (EE 288) group assignment at KNUST, Department of Computer Engineering.

## Project highlights

- Captures temperature and humidity using a DHT11 sensor
- Monitors ambient light with an LDR
- Measures distance/proximity with an ultrasonic sensor
- Publishes sensor readings from an ESP32 through MQTT (Mosquitto)
- Visualizes live readings and historical trends with Python Dash
- Provides threshold-based visual alerts and ESP32 built-in LED feedback

## System architecture

```text
DHT11 / LDR / Ultrasonic sensors
              |
              v
            ESP32
              |
              v
       MQTT broker (Mosquitto)
              |
              v
       Python Dash application
              |
              v
      Live web dashboard and alerts
              |
              v
        ESP32 built-in LED feedback
```

## Dashboard features

- Four live gauges for temperature, humidity, light, and distance
- Four real-time line graphs for monitoring sensor trends
- Dynamic colour indicators for light and proximity readings
- Threshold-based alerts for readings that need attention
- Dark-themed dashboard interface
- Hardware feedback through the ESP32 built-in LED

## Tech stack

- **Hardware:** ESP32, DHT11, LDR, ultrasonic sensor
- **Embedded development:** Arduino IDE / C++
- **Messaging:** MQTT with Mosquitto
- **Dashboard:** Python, Dash, Plotly

## Getting started

### Prerequisites

- An ESP32 configured with the connected sensors
- Arduino IDE with ESP32 board support
- A running Mosquitto MQTT broker
- Python 3

### 1. Install the Python dependencies

```bash
pip install -r requirements.txt
```

### 2. Configure and upload the ESP32 firmware

1. Open `LAB3_MQTT.ino` in the Arduino IDE.
2. Update the Wi-Fi credentials and MQTT broker IP address to match your network.
3. Select the correct ESP32 board and port, then upload the sketch.

### 3. Start the MQTT broker

Start Mosquitto on the machine or network where it is installed. On Windows, if Mosquitto is installed as a service, this may be done with:

```bash
net start mosquitto
```

### 4. Run the dashboard

```bash
python dashboard.py
```

Then open [http://127.0.0.1:8050](http://127.0.0.1:8050) in your browser.

## My contribution

This was completed as an EE 288 group assignment. I independently implemented the complete technical solution, including:

- ESP32 firmware development and sensor integration
- MQTT-based communication between the ESP32 and dashboard
- Python Dash dashboard development and real-time data visualisation
- Threshold-based alerts and ESP32 LED feedback
- End-to-end integration, testing, and configuration of the monitoring pipeline

## Team

**Group μ (12)**

- Darko Alex Ohene — 4095424
- Nana Yaa Ofosuwaa Tenkorang — 4109524
- Kunsu Hammond Tietaa — 4101224
- Kwesi Ohene Gvan — 4098424

## Course

**Electrical Measurement and Instrumentation (EE 288)**  
KNUST — Department of Computer Engineering

## License

This project is licensed under the [MIT License](LICENSE).
nder the [MIT License](LICENSE).
