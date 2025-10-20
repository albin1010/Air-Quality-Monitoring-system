# IoT-Based Air Quality Monitoring System

This project implements a compact, low-cost system for real-time monitoring of air quality, temperature, and humidity, utilizing the **ESP8266 NodeMCU** and the **Blynk 2.0 Cloud Platform**.

The system continuously measures air quality by detecting harmful gases such as $\text{NH}_3$, $\text{NO}_{\text{x}}$, $\text{CO}_2$, smoke, and benzene.

## 🎥 Comprehensive Project Demonstration

Demonstrating the operational workflow, real-time data capture, and automated alarm sequences of the monitoring system.

**Clickable Video Demonstration**
<br>
<a href="https://drive.google.com/file/d/1PKbk-TQ3kxujMSxxviOvx8rL3FXMY_Bh/view?usp=drivesdk">
  <img src="Diagrams/demo-thumbnail.jpg" alt="Click to Watch Video Demonstration" width="600" />
</a>

***

## 🌟 Key Features

* **Real-time Monitoring:** Measures air quality using the **MQ-135 Gas Sensor** (connected to A0) and environmentals (T/H) using the **DHT11 Sensor** (connected to D4).
* **Remote Visualization:** Sensor data is transmitted via Wi-Fi to the **Blynk Cloud Dashboard** for real-time and historical trend plotting.
* **Local & Remote Alerts:** Triggers a local **Buzzer** (D0) and **LED** (D6) alarm when pollutant concentration exceeds a set threshold (e.g., 250 PPM), and generates mobile alerts via Blynk.
* **Compensation:** The firmware applies environmental compensation logic using temperature and humidity readings to improve the accuracy of the gas sensor's PPM calculation.

## 🛠️ Project Structure and Components

The repository is organized into three main folders:

| Folder | Content |
| :--- | :--- |
| **[`Firmware/`](Firmware/)** | Contains the Arduino/ESP8266 source code (`.ino` file). |
| **[`Diagrams/`](Diagrams/)** | Contains the circuit and block diagram images. |
| **[`Docs/`](Docs/)** | Contains the full micro-project report (PDF). |

### Pin Configuration

| Component | NodeMCU Pin | Notes |
| :--- | :--- | :--- |
| **MQ-135 Analog Out** | A0 | Analog sensor reading |
| **DHT11 Data** | D4 | Digital data pin |
| **Buzzer** | D0 | Buzzer control (active LOW) |
| **Alarm LED** | D6 | Physical LED indicator |

## 🔗 Project Files

* **Full Report (PDF):** [Docs/Air\_Quality\_Monitoring\_System\_Report.pdf](Docs/Air_Quality_Monitoring_System_Report.pdf)
* **Code (`.ino`):** [Firmware/air\_quality\_monitor\_blynk.ino](Firmware/air_quality_monitor_blynk.ino)
* **Block Diagram:** [Diagrams/Block\_Diagram\_Image.jpg](Diagrams/Block_Diagram_Image.jpg)
* **Circuit Diagram:** [Diagrams/Circuit\_Diagram\_Image.jpg](Diagrams/Circuit_Diagram\_Image.jpg)
* 
