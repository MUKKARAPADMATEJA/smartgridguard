# ⚡ Smart Grid Guard: IoT-Based Power Monitoring System

[![Tinkercad Simulation](https://img.shields.io/badge/Tinkercad-View_Live_Circuit-orange?style=for-the-badge&logo=autodesk)](https://www.tinkercad.com/things/8YDH8Py2s8M-smart-grid-guard)

**Independently Developed By:** Mukkara Padma Teja  
**🔗 Live Circuit Simulation:** [Smart Grid Guard on Tinkercad](https://www.tinkercad.com/things/8YDH8Py2s8M-smart-grid-guard)

---

## 📌 Overview
Electrical power systems often experience voltage fluctuations and unexpected faults, leaving users unaware until equipment damage or power interruptions occur. **Smart Grid Guard** solves this by continuously monitoring voltage conditions in real time and providing immediate local and remote alerts whenever abnormal situations are detected.

---

## 🚀 Key Features
* **Real-Time Voltage Monitoring:** Continuously tracks voltage variations and analyzes grid risk levels.
* **Local Visual & Audible Alerts:** 
  * 🟢 **Normal Condition:** Green LED glows and LCD displays normal status (`Grid: 230V OK / Risk: LOW`).
  * 🟡 **Warning Condition:** Yellow LED glows and LCD displays a warning message.
  * 🔴 **Critical Fault Condition:** Red LED and Piezo Buzzer activate simultaneously with a critical fault alert on the LCD.
* **Remote Telegram Notifications:** A Python script reads Arduino serial data and sends instant warning/fault notifications to the user via a Telegram Bot.

---

## 🛠️ Components Used

| Component | Purpose |
| :--- | :--- |
| **Arduino Uno** | Controls the entire system and processes voltage readings |
| **16×2 I2C LCD Display** | Displays real-time system status and risk levels |
| **Potentiometer** | Simulates voltage fluctuations on an analog input pin |
| **Green, Yellow & Red LEDs** | Indicates Normal, Warning, and Fault conditions |
| **Piezo Buzzer** | Provides audible alerts during critical fault conditions |
| **Breadboard & Jumper Wires** | Connects all circuit components without soldering |

---

## 🔄 System Architecture & Workflow

```text
[Potentiometer (Voltage Input)] 
       ↓
 [Arduino Uno (Condition Analysis)]
       ├──► [16x2 I2C LCD Display]
       ├──► [Green / Yellow / Red LEDs]
       ├──► [Piezo Buzzer Alert]
       ↓ (Serial Communication)
 [Python Script]
       ↓
 [Telegram Bot API]
       ↓
 [Instant User Notification]
