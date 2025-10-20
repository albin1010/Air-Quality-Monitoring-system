# IoT-Based Air Quality Monitoring System

This project implements a compact, low-cost system for real-time monitoring of air quality, temperature, and humidity, utilizing the **ESP8266 NodeMCU** and the **Blynk 2.0 Cloud Platform**.

The system continuously measures air quality by detecting harmful gases such as $\text{NH}_3$, $\text{NO}_{\text{x}}$, $\text{CO}_2$, smoke, and benzene.

## 🎥 Comprehensive Project Demonstration

Demonstrating the operational flow, real-time data capture, and automated alarm sequences of the monitoring system.

<p align="center">
  <a href="https://drive.google.com/file/d/1PKbk-TQ3kxujMSxxviOvx8rL3FXMY_Bh/view?usp=drivesdk">
    <img src="Diagrams/demo-thumbnail.jpg" alt="Click to Watch Video Demonstration" width="70%" />
  </a>
  <br>
  [Click to Launch Full HD Demonstration on Google Drive]
</p>

---
*Note on Access: The demonstration video is hosted externally to comply with GitHub's file size restrictions. Please ensure public access permissions are active on the Google Drive link.*

***

## 🌟 Key Features

* **Real-time Monitoring:** Measures air quality using the **MQ-135 Gas Sensor** (connected to A0) and environmentals (T/H) using the **DHT11 Sensor** (connected to D4).
* **Remote Visualization:** Sensor data is transmitted via Wi-Fi to the **Blynk Cloud Dashboard** for real-time and historical trend plotting.
* **Local & Remote Alerts:** Triggers a local **Buzzer** (D0) and **LED** (D6) alarm when pollutant concentration exceeds a set threshold (e.g., 250 PPM), and generates mobile alerts via Blynk.
* **Compensation:** The firmware applies environmental compensation logic using temperature and humidity readings to improve the accuracy of the gas sensor's PPM calculation.

... (rest of your file content)
