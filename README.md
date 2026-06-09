# Healthily ☀️❤️
### Low-Cost Solar-Charged Wearable for Remote Patient Vitals Monitoring

> Continuous health monitoring, powered by sunlight — built for India.

<p align="center">
  <img src="images/healthily_main.jpg" alt="Healthily Wearable Device" width="700"/>
  <br/>
  <em>Healthily — Solar-powered wearable health monitoring band</em>
</p>

---

## 📌 Overview

**Healthily** is a low-cost, solar-powered wearable health monitoring device designed for remote and underserved patient populations. It continuously tracks multiple vital parameters — including heart rate, SpO2, ECG, and fall detection — while using ambient solar energy harvesting to dramatically extend battery life without frequent charging.

The device supports **multi-modal data transmission** including Wi-Fi and NRF radio modules, making it viable in both urban and rural settings with or without internet infrastructure.

---

## 🔥 The Problem

<p align="center">
  <img src="images/problem_stats.jpg" alt="Problem Statistics" width="650"/>
</p>

- **64.5%** of smart wearable owners recharge their devices 2–3 times per week, creating critical **data gaps** in continuous monitoring
- **838,300 people** died in India in 2018 due to insufficient healthcare access
- NCDs (cardiovascular diseases, respiratory disorders) account for **~67.6% of all deaths** in India
- Battery production contributes to **45% of China's greenhouse gas emissions**
- Existing wearables are priced out of reach for rural and low-income patients

---

## ✨ Features

| Feature | Details |
|---|---|
| ❤️ Heart Rate + SpO2 | Industrial-grade **MAX30102** sensor (near radial artery) |
| 🫀 ECG Monitoring | Real-time **3-lead ECG** from finger-based probe using AD8232 |
| ☀️ Solar Charging | Integrated solar panel — generates ~**50mA/day** ambient light harvesting |
| ⚡ Ultra-Low Power | STM32 + optimized sleep modes for extended runtime |
| 📡 Multi-Modal Transmission | ESP32 (Wi-Fi/BT) + NRF module (for areas with no server access) |
| 🤸 Fall Detection | MPU6050 accelerometer-based fall detection |

---

## 🛠️ Hardware Architecture

<p align="center">
  <img src="images/hardware_overview.jpg" alt="Hardware Components" width="700"/>
  <br/>
  <em>Complete hardware stack — MCUs, sensors, solar panel, and power management</em>
</p>

### Finger-Based ECG Probe

<p align="center">
  <img src="images/ecg_probe.jpg" alt="Finger ECG Probe" width="500"/>
  <br/>
  <em>Custom finger-based 3-lead ECG probe using AD8232</em>
</p>

### Solar Energy Harvesting

<p align="center">
  <img src="images/solar_panel.jpg" alt="Solar Panel Integration" width="500"/>
  <br/>
  <em>Integrated solar panel with STM32 + Buck converter + charging module stack</em>
</p>

### Component Breakdown

| Component | Role | Power Consumption | Cost |
|---|---|---|---|
| STM32F401CCU6 | Main MCU (ultra-low power) | Sleep: 2–8mA / Active: 10–25mA | ₹300 |
| ESP32 | Data communicator (Wi-Fi/BT) | Sleep: 2–8mA / Active: 80–250mA | ₹300 |
| MAX30102 | Heart Rate + SpO2 | Sleep: 0.7µA / Active: 600–800µA | ₹150 |
| AD8232 | ECG (finger probe) | Sleep: 1µA / Active: 170µA | ₹350 |
| SSD1306 | OLED Display | Sleep: 2–5mA / Active: 25–30mA | ₹120 |
| MPU6050 | Fall Detection | Accel only: 6.5µA / Both: 3.9mA | ₹100 |
| Buck/Booster + Misc | Power management | — | ₹400 |
| **Total** | | **~76.9 mA/day** | **₹1,720** |

---

## ⚡ Battery Life

<p align="center">
  <img src="images/battery_comparison.jpg" alt="Battery Life Comparison" width="550"/>
</p>

| Mode | Runtime |
|---|---|
| Without Solar | ~**6.5 days** |
| With Solar Harvesting | ~**12 days** |

> 🟢 **3x lower cost** than comparable commercial wearable brands

---

## 📊 Vitals Monitored

<p align="center">
  <img src="images/vitals_dashboard.jpg" alt="Vitals Monitoring Dashboard" width="600"/>
  <br/>
  <em>Real-time vitals display on OLED + data transmitted to cloud/NRF</em>
</p>

1. Heart Rate (BPM)
2. SpO2 (Blood Oxygen Saturation)
3. 3-Lead ECG
4. Body Temperature
5. Fall Detection
6. Activity / Motion Data

---

## 🔮 Future Work

- Integrate **blood pressure monitoring** into the band
- Develop **RF/LoRa communication** for rural areas without internet infrastructure
- Deploy a **ground station** for remote hospital-grade patient monitoring
- AI/ML integration for **arrhythmia and sleep apnea** detection
- **ADP5092** for indoor light voltage boosting in solar panels
- Customizable configurations for elderly patients

---

## 📈 Market Potential

<p align="center">
  <img src="images/market.jpg" alt="Market Analysis" width="600"/>
</p>

- Global smart wearable market: **$385.5 Billion by 2032** (CAGR: 15.3%)
- India's wearable device market grew **34%** in 2023 to **134 Million Units** (IDC)
- Primary targets: Remote patients, elderly individuals, rural clinics, hospitals

---

## 🏆 Recognition

<p align="center">
  <img src="images/awards.jpg" alt="Awards and Recognitions" width="600"/>
  <br/>
  <em>Team Healthily across competitions</em>
</p>

- 🥇 **NIT Hackathon 2025** — Winner
- 🥇 **Adinova MMC 2025** — Winner
- 🏅 **Apollo Solvathon, IIT Delhi** — Finalist

---

## 👥 Team

<p align="center">
  <img src="images/team.jpg" alt="Team Healthily" width="600"/>
</p>

| Name | Branch | Background |
|---|---|---|
| Anurag Biswas | B.Tech CSE, Adamas University | DGCA Certified Drone Pilot |
| Sumanto Roy | B.Tech EE, Adamas University | Observer — Plastic & Reconstructive Microsurgery, Ganga Hospital |
| Soumyadeep Das | B.Tech CSE, Adamas University | DGCA Certified Drone Pilot |

---

## 📁 Image Guide

> Add your photos to an `images/` folder in the root of this repo and name them as below:

| Filename | What to put |
|---|---|
| `images/healthily_main.jpg` | Full device photo / wrist shot |
| `images/problem_stats.jpg` | Problem slide screenshot or infographic |
| `images/hardware_overview.jpg` | All components laid out flat |
| `images/ecg_probe.jpg` | Finger ECG probe photo |
| `images/solar_panel.jpg` | Solar panel + charging circuit photo |
| `images/battery_comparison.jpg` | Battery life chart or slide screenshot |
| `images/vitals_dashboard.jpg` | OLED display showing live readings |
| `images/market.jpg` | Market growth chart |
| `images/awards.jpg` | Awards/event photos from NIT Hackathon, Adinova MMC, or Apollo Solvathon |
| `images/team.jpg` | Team photo |

---

## 📜 License

© 2024 Anurag Biswas, Sumanto Roy, Soumyadeep Das. All rights reserved.

This project and all associated hardware designs, firmware, software, and documentation are the intellectual property of the team. No part of this project may be reproduced, distributed, modified, or used in any form without explicit written permission from the authors.

---

> *"Keeping patients connected to care — wherever they are, powered by the sun."*
