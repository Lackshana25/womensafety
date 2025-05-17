
This project is an **IoT-based real-time Women Safety System** developed using **ESP32**, **ESP32-CAM**, **GSM**, **GPS**, and sensor technologies. It aims to provide immediate response in emergency situations through automated alerts, location tracking, and live streaming features.

---

 Features

- 🔊 **Sound Sensor** detects distress noise
- ✋ **Touch Sensor** detects aggressive contact
- 🔘 **Manual Push Button** for SOS activation
- 📍 **GPS (NEO-6M)** for real-time location tracking
- 📱 **GSM (SIM900A)** module for sending:
  - Emergency **SMS with live location**
  - Automatic **calls to emergency contacts**
- 📷 ESP32-CAM captures image of intruder and emails it
- 📡 ESP-NOW protocol enables wireless trigger to ESP32-CAM
- 📧 Sends **streaming URL** via email for live surveillance
- 📺 **LCD Display** shows alert status and two-way SMS updates

---

## 🔧 Components Used

- ESP32
- ESP32-CAM
- SIM900A GSM Module
- NEO-6M GPS Module
- Sound Sensor
- Touch Sensor
- Push Buttons
- LCD Display (I2C)
- SMTP (for email alerts)

---
 ⚙️ How It Works

1. The system constantly monitors the environment using sound and touch sensors.
2. On detection of abnormal activity or manual alert press:
   - Location is fetched via GPS
   - GSM sends an SMS with a Google Maps link
   - GSM also initiates calls to preset contacts
   - ESP32 triggers ESP32-CAM using ESP-NOW
   - ESP32-CAM captures image and sends via email
   - Then starts a live video stream and emails the stream URL
3. LCD display updates alert status and incoming reply SMS messages (2-way GSM communication)
