# IoT-Based Air Quality Monitoring System

[span_0](start_span)This project implements a compact, low-cost system for real-time monitoring of air quality, temperature, and humidity, utilizing the **ESP8266 NodeMCU** and the **Blynk 2.0 Cloud Platform**[span_0](end_span).

[span_1](start_span)The system continuously measures air quality by detecting harmful gases such as **NH₃**, **NOₓ**, **CO₂**, smoke, and benzene[span_1](end_span). [span_2](start_span)The collected data is transmitted via Wi-Fi to the cloud platform (Blynk), where it can be visualized on a real-time dashboard and monitored remotely[span_2](end_span).

## 🎥 Comprehensive Project Demonstration

Demonstrating the operational workflow, real-time data capture, and automated alarm sequences of the monitoring system.

**[File Size Limit Exceeded: Click to View Demonstration Externally]**
<br>
<a href="https://drive.google.com/file/d/1PKbk-TQ3kxujMSxxviOvx8rL3FXMY_Bh/view?usp=drivesdk">
  <img src="Diagrams/demo-thumbnail.jpg" alt="Click to Watch Video Demonstration" width="600" />
</a>

***

## 🌟 Key Features

* **[span_3](start_span)Real-time Monitoring:** Measures air quality using the **MQ-135 Gas Sensor** (connected to A0) and environmentals (T/H) using the **DHT11 Sensor** (connected to D4)[span_3](end_span).
* **[span_4](start_span)[span_5](start_span)Remote Visualization & Scalability:** Data is transmitted via Wi-Fi to the **Blynk Cloud Dashboard** for visualization and is scalable to multiple nodes[span_4](end_span)[span_5](end_span).
* **[span_6](start_span)[span_7](start_span)Local & Remote Alerts:** Triggers a local **Buzzer** (D0) and **LED** (D6) alarm when pollutant concentration exceeds a set threshold (e.g., 250 PPM)[span_6](end_span)[span_7](end_span)[span_8](start_span), and generates mobile alerts via Blynk[span_8](end_span).
* **[span_9](start_span)[span_10](start_span)Compensation Logic:** The firmware reads temperature and humidity from the DHT11 for environmental compensation of gas readings, improving the accuracy of the gas sensor's PPM calculation[span_9](end_span)[span_10](end_span).

## 💻 Interfacing and Logic Summary

[span_11](start_span)The core program runs on the NodeMCU and manages the system's functions[span_11](end_span):
* [span_12](start_span)[span_13](start_span)Reads the gas sensor's analog value, calculates resistance, and converts it to PPM[span_12](end_span)[span_13](end_span).
* [span_14](start_span)Controls the buzzer and LED alarm based on PPM exceeding the threshold[span_14](end_span).
* [span_15](start_span)Sends readings (temperature, humidity, and PPM) to Blynk app virtual pins for real-time display[span_15](end_span).
* [span_16](start_span)Uses a timer to periodically read sensors every 5 seconds[span_16](end_span).

### Pin Configuration

| Component | NodeMCU Pin | Notes |
| :--- | :--- | :--- |
| **MQ-135 Analog Out** | A0 | [span_17](start_span)Analog sensor reading[span_17](end_span) |
| **DHT11 Data** | D4 | [span_18](start_span)Digital data pin[span_18](end_span) |
| **Buzzer** | D0 | [span_19](start_span)Buzzer control (active LOW)[span_19](end_span) |
| **Alarm LED** | D6 | [span_20](start_span)Physical LED indicator[span_20](end_span) |

### Validation and Results

| Parameter | Expected | Observed |
| :--- | :--- | :--- |
| **Temperature display** | [span_21](start_span)Real-time on Blynk, ±2°C accuracy[span_21](end_span) | [span_22](start_span)Accurate (±1.5°C)[span_22](end_span) |
| **Air quality reading (PPM)** | [span_23](start_span)Accurate pollution indication (PPM)[span_23](end_span) | [span_24](start_span)Consistent, reliable with valid baseline[span_24](end_span) |
| **Buzzer/LED alarm** | [span_25](start_span)Activates above 250 PPM[span_25](end_span) | [span_26](start_span)Triggers reliably on alarm, silent otherwise[span_26](end_span) |
| **Wi-Fi connectivity** | [span_27](start_span)Stable, auto reconnect[span_27](end_span) | [span_28](start_span)Short disconnects handled, quickly reconnects[span_28](end_span) |

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
