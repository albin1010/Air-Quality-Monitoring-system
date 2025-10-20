# IoT-Based Air Quality Monitoring System

[span_0](start_span)[span_1](start_span)This project implements a compact, low-cost system for real-time monitoring of air quality, temperature, and humidity[span_0](end_span)[span_1](end_span)[span_2](start_span)[span_3](start_span), utilizing the **ESP8266 NodeMCU** and the **Blynk 2.0 Cloud Platform**[span_2](end_span)[span_3](end_span).

[span_4](start_span)[span_5](start_span)The system continuously measures air quality by detecting harmful gases such as $\text{NH}_3$, $\text{NO}_{\text{x}}$, $\text{CO}_2$, smoke, and benzene[span_4](end_span)[span_5](end_span).

## 🌟 Key Features

* **[span_6](start_span)[span_7](start_span)Real-time Monitoring:** Measures air quality using the **MQ-135 Gas Sensor** (connected to A0) and environmentals (T/H) using the **DHT11 Sensor** (connected to D4)[span_6](end_span)[span_7](end_span).
* **[span_8](start_span)[span_9](start_span)[span_10](start_span)Remote Visualization:** Sensor data is transmitted via Wi-Fi to the **Blynk Cloud Dashboard** for real-time and historical trend plotting[span_8](end_span)[span_9](end_span)[span_10](end_span).
* **[span_11](start_span)[span_12](start_span)[span_13](start_span)[span_14](start_span)Local & Remote Alerts:** Triggers a local **Buzzer** (D0) and **LED** (D6) alarm when pollutant concentration exceeds a set threshold (e.g., 250 PPM), and generates mobile alerts via Blynk[span_11](end_span)[span_12](end_span)[span_13](end_span)[span_14](end_span).
* **[span_15](start_span)Compensation:** The firmware applies environmental compensation logic using temperature and humidity readings to improve the accuracy of the gas sensor's PPM calculation[span_15](end_span).

## 🛠️ Project Structure and Components

The repository is organized into three main folders:

| Folder | Content |
| :--- | :--- |
| **[`Firmware/`](Firmware/)** | [span_16](start_span)[span_17](start_span)Contains the Arduino/ESP8266 source code (`.ino` file)[span_16](end_span)[span_17](end_span). |
| **[`Diagrams/`](Diagrams/)** | [span_18](start_span)Contains the circuit and block diagram images[span_18](end_span). |
| **[`Docs/`](Docs/)** | [span_19](start_span)Contains the full micro-project report (PDF)[span_19](end_span). |

### Pin Configuration

| Component | NodeMCU Pin | Notes |
| :--- | :--- | :--- |
| **MQ-135 Analog Out** | A0 | [span_20](start_span)[span_21](start_span)[span_22](start_span)Analog sensor reading[span_20](end_span)[span_21](end_span)[span_22](end_span) |
| **DHT11 Data** | D4 | [span_23](start_span)[span_24](start_span)Digital data pin[span_23](end_span)[span_24](end_span) |
| **Buzzer** | D0 | [span_25](start_span)[span_26](start_span)Local alert indicator (active LOW)[span_25](end_span)[span_26](end_span) |
| **Alarm LED** | D6 | [span_27](start_span)[span_28](start_span)Physical LED indicator[span_27](end_span)[span_28](end_span) |

## 🔗 Project Files

* **Full Report (PDF):** [Docs/Air\_Quality\_Monitoring\_System\_Report.pdf](Docs/Air_Quality_Monitoring_System_Report.pdf)
* **Code (`.ino`):** [Firmware/air\_quality\_monitor\_blynk.ino](Firmware/air_quality_monitor_blynk.ino)
* **Block Diagram:** [Diagrams/Block\_Diagram\_Image.jpg](Diagrams/Block_Diagram_Image.jpg)
* **Circuit Diagram:** [Diagrams/Circuit\_Diagram\_Image.jpg](Diagrams/Circuit_Diagram_Image.jpg)
* 
