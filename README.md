
# 🔭 Radar Defense Project

An Arduino-powered **Radar Detection and Alert System** capable of detecting nearby objects using an ultrasonic sensor, triggering visual/audio alerts, sending **Telegram notifications**, and **logging real-time data** into a CSV file. Perfect for defense simulation, robotics, or security systems.

---

## 📦 Features

- 🚨 **Distance-based LED & Buzzer Alerts**
  - Green LED: Safe Zone
  - Yellow LED: Caution Zone
  - Red LED + Buzzer: Danger Zone (object < critical distance)

- 📈 **Real-Time Radar Scanning Visualization**
  - Graphical sweep display with the closest object highlighted
  - Flashing ring animation for the closest object

- 📲 **Instant Telegram Notification**
  - Sends alert when an object is detected under 10 cm

- 📂 **CSV Data Logging**
  - Logs distance, angle, timestamp, and object status

---

## 🔧 Hardware Used

| Component            | Description                     |
|---------------------|---------------------------------|
| Arduino Uno         | Microcontroller Board           |
| HC-SR04 Sensor      | Ultrasonic Distance Sensor      |
| LEDs (Red/Yellow/Green) | Visual Alert Indicators    |
| Buzzer              | Audio Alert                     |
| Jumper Wires        | For Connections                 |
| Breadboard          | Prototyping                     |

### 🔌 Pin Connections

| Component       | Arduino Pin |
|----------------|-------------|
| Trig (Ultrasonic) | D8       |
| Echo (Ultrasonic) | D9       |
| Red LED         | D12        |
| Yellow LED      | D6         |
| Green LED       | D7         |
| Buzzer          | D11        |

---

## 🧠 Software Components

- **Arduino IDE** for hardware control
- **Python (telegram_alert.py)** for sending Telegram messages
- **CSV Logger** for recording real-time sensor data
- **Graphical Visualization** (processing.py / GUI frontend)

---

## 🚀 How It Works

1. Ultrasonic sensor scans for objects using sound waves.
2. Based on distance:
   - LEDs and buzzer provide real-time alerts.
   - Data is logged in a CSV file.
3. If the distance is less than 10 cm:
   - A Telegram bot sends an alert to the user instantly.
4. The closest object is visually highlighted on the radar.

---
