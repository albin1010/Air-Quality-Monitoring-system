# IoT-Based Air Quality Monitoring System

This project implements a compact, low-cost system for real-time monitoring of air quality, temperature, and humidity, utilizing the **ESP8266 NodeMCU** and the **Blynk 2.0 Cloud Platform**.

The system continuously measures air quality by detecting harmful gases such as **NH₃**, **NOₓ**, **CO₂**, smoke, and benzene. The collected data is transmitted via Wi-Fi to the cloud platform (Blynk), where it can be visualized on a real-time dashboard and monitored remotely.

## 🎥 Comprehensive Project Demonstration

Demonstrating the operational workflow, real-time data capture, and automated alarm sequences of the monitoring system.

**[Click Image to Watch Full System Demonstration Video]**
<br>
<a href="https://drive.google.com/file/d/1PKbk-TQ3kxujMSxxviOvx8rL3FXMY_Bh/view?usp=drivesdk">
  <img src="Diagrams/demo-thumbnail.jpg" alt="Click to Watch Video Demonstration" width="600" />
</a>

***

## 🌟 Key Features

* **Real-time Monitoring:** Measures air quality using the **MQ-135 Gas Sensor** (connected to A0) and environmentals (T/H) using the **DHT11 Sensor** (connected to D4).
* **Remote Visualization & Scalability:** Data is transmitted via Wi-Fi to the **Blynk Cloud Dashboard** for visualization and is scalable to multiple nodes.
* **Local & Remote Alerts:** Triggers a local **Buzzer** (D0) and **LED** (D6) alarm when pollutant concentration exceeds a set threshold (e.g., 250 PPM), and generates mobile alerts via Blynk.
* **Compensation Logic:** The firmware reads temperature and humidity from the DHT11 for environmental compensation of gas readings, improving the accuracy of the gas sensor's PPM calculation.

## 💻 Interfacing and Logic Summary

The core program runs on the NodeMCU and manages the system's functions:
* Reads the gas sensor's analog value, calculates resistance, and converts it to PPM.
* Controls the buzzer and LED alarm based on PPM exceeding the threshold.
* Sends readings (temperature, humidity, and PPM) to Blynk app virtual pins for real-time display.
* Uses a timer to periodically read sensors every 5 seconds.

### Pin Configuration

| Component | NodeMCU Pin | Notes |
| :--- | :--- | :--- |
| **MQ-135 Analog Out** | A0 | Analog sensor reading |
| **DHT11 Data** | D4 | Digital data pin |
| **Buzzer** | D0 | Buzzer control (active LOW) |
| **Alarm LED** | D6 | Physical LED indicator |

### Validation and Results

| Parameter | Expected | Observed |
| :--- | :--- | :--- |
| **Temperature display** | Real-time on Blynk, ±2°C accuracy | Accurate (±1.5°C) |
| **Air quality reading (PPM)** | Accurate pollution indication (PPM) | Consistent, reliable with valid baseline |
| **Buzzer/LED alarm** | Activates above 250 PPM | Triggers reliably on alarm, silent otherwise |
| **Wi-Fi connectivity** | Stable, auto reconnect | Short disconnects handled, quickly reconnects |

## 🛠️ Project Structure and Components

The repository is organized into three main folders:

| Folder | Content |
| :--- | :--- |
| **[`Firmware/`](Firmware/)** | Contains the Arduino/ESP8266 source code (`.ino` file). |
| **[`Diagrams/`](Diagrams/)** | Contains the circuit and block diagram images. |
| **[`Docs/`](Docs/)** | Contains the full micro-project report (PDF). |

## 🔗 Project Files

* **Full Report (PDF):** [Docs/Air\_Quality\_Monitoring\_System\_Report.pdf](Docs/Air_Quality_Monitoring_System_Report.pdf)
* **Code (`.ino`):** [Firmware/air\_quality\_monitor\_blynk.ino](Firmware/air_quality_monitor_blynk.ino)
* **Block Diagram:** [Diagrams/Block\_Diagram\_Image.jpg](Diagrams/Block_Diagram_Image.jpg)
* **Circuit Diagram:** [Diagrams/Circuit\_Diagram\_Image.jpg](Diagrams/Circuit_Diagram\_Image.jpg)
