# ❄️ UrbanCool — AI-Driven Responsive Cooling System

### Cooling Smarter. Living Better.

UrbanCool is an AI-driven framework for responsive urban cooling, designed to address the **Urban Heat Island (UHI)** effect while improving energy efficiency and thermal comfort.

The project combines multi-source urban data, predictive modeling, and adaptive cooling control to demonstrate how cooling infrastructure can move from **reactive operation to predictive and adaptive management**.

> 🎓 **Research Publication:** IEEE Xplore  
> 📄 **Paper:** AI for Environmental Management: UrbanCool – AI-Driven Responsive Cooling System  
> 🏛️ **Conference:** 2026 IEEE International Conference for Convergence in Computing Technology (I3CTCON)  
> 🆔 **Paper ID:** 1017  
> 🔗 **DOI:** 10.1109/I3CTCON68242.2026.11507747
> 🔗**URL:** https://ieeexplore.ieee.org/document/11507747
---

## 📌 About the Research

Rapid urbanization contributes to rising temperatures, increased energy consumption, and heat-related risks. Traditional urban cooling systems commonly rely on fixed schedules or limited sensor inputs, making them inefficient when environmental conditions and crowd density change.

**UrbanCool** proposes a responsive cooling framework that combines:

- 🌦️ Weather and environmental data
- 🌡️ IoT sensor information
- 👥 Crowd-density estimation
- 📅 Event metadata
- 🧠 Predictive temperature modeling
- 🤖 Reinforcement learning-based cooling control

The system identifies areas with higher cooling demand and dynamically determines where cooling resources should be activated.

---

## 🏗️ System Workflow

```text
Weather Data ───────┐
IoT Sensors ────────┤
Crowd Data ─────────┤
Event Metadata ─────┘
          │
          ▼
┌──────────────────────────┐
│ Data Processing & Fusion │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│   Prediction Engine      │
│   LSTM / Time-Series     │
│   Forecasting            │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│ Control & Optimization   │
│   RL / DQN Strategy      │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│ Cooling Infrastructure   │
│                          │
│ • Misting Stations       │
│ • Solar-Powered Fans     │
│ • Smart Shading          │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│ Feedback & Adaptation    │
└────────────┬─────────────┘
             │
             └──────► Continuous Optimization
````

---

## 🧠 Research Approach

UrbanCool follows a five-layer architecture:

### 1. Data Collection

The framework considers multiple urban data sources:

* Weather forecasts
* Temperature and humidity sensors
* Air-quality measurements
* WiFi / cellular crowd-density signals
* Public event information

### 2. Data Processing & Fusion

The collected information is cleaned, normalized, synchronized, and combined into a unified representation.

Key features include:

* Temperature
* Humidity
* AQI
* Crowd density
* Temperature change rate
* Crowd change rate

### 3. Prediction Engine

The research uses **LSTM-based time-series forecasting** to predict short-term temperature changes.

The study compares the predictive approach against traditional models including:

* Linear Regression
* ARIMA
* LSTM

### 4. Adaptive Control

A **Deep Q Network (DQN)** is used in the research framework to determine cooling activation policies.

The control objective is to balance:

* Thermal comfort
* Energy consumption
* Cooling demand

### 5. Feedback & Adaptation

The system continuously evaluates:

* Temperature changes
* Energy consumption
* Thermal comfort
* Cooling effectiveness

The feedback can then be used to improve future decisions.

---

# 🖥️ Streamlit Prototype

This repository contains a **Streamlit-based proof-of-concept prototype** of the UrbanCool framework.

The prototype provides an interactive simulation of the system workflow and demonstrates how environmental conditions, crowd density, cooling resources, energy consumption, and system resilience can be visualized.

### ⚠️ Prototype Scope

The current Streamlit application is a **simulation and visualization prototype**.

Its data is simulated and does not require external API keys or physical IoT hardware.

The prototype demonstrates the **concept and architecture** presented in the research rather than representing a full-scale real-world deployment.

---

## ✨ Prototype Features

### 📊 Interactive Dashboard

Monitor and control the simulated UrbanCool environment through a clean Streamlit interface.

### 🌆 Multi-City Simulation

Simulate different urban environments:

* Delhi
* Mumbai
* Pune
* Bangalore

### 🔄 Dynamic Data Fusion

The prototype combines simulated:

* Weather conditions
* Heat-island conditions
* Crowd-density signals
* Environmental parameters

to identify **"hot + crowded" zones**.

### 🧠 AI Prediction Simulation

Demonstrates how the prediction layer can identify areas with increased cooling demand based on the fused environmental information.

### 🗺️ Cooling Device Control Map

Interactive Folium maps visualize cooling infrastructure such as:

* Misting fountains
* Shade sails
* Cooling units

and their simulated activation intensity.

### ⚡ Energy Monitoring

Plotly visualizations compare:

* Baseline energy consumption
* UrbanCool energy consumption
* Cooling performance

### 🔁 Feedback Loop

The dashboard visualizes the relationship between:

```text
Cooling Action
      ↓
Temperature Change
      ↓
Energy Consumption
      ↓
System Feedback
      ↓
Next Decision
```

### 🚨 Anomaly & Resilience Simulation

The prototype can simulate system anomalies such as:

* Sensor failure
* Data irregularities
* Cooling-system interruptions

and demonstrate fallback control behavior.

### 📈 Scalability Simulation

The prototype provides a conceptual view of how the system could be expanded across:

* Multiple neighborhoods
* Different urban zones
* Additional cooling assets

---

# 📈 Research Results

The experimental study reported the following results:

| System            | Prediction Accuracy | Energy Savings | Avg. Comfort Index |
| ----------------- | ------------------: | -------------: | -----------------: |
| Static Cooling    |               78.2% |             0% |             27.5°C |
| Rule-Based System |               85.1% |            18% |             25.9°C |
| **UrbanCool**     |           **92.4%** |        **35%** |         **24.2°C** |

Additional reported outcomes include:

* **0.74°C MAE** for LSTM temperature forecasting
* **0.96°C RMSE**
* **3.5°C average zone temperature reduction**
* Energy consumption reduced from **4.8 kWh/day to 3.1 kWh/day**
* Thermal Comfort Index maintained within the comfort range for **91% of operational time**

These results are from the research evaluation and simulation described in the published paper.

---

# 🛠️ Technology Stack

| Category        | Technology               |
| --------------- | ------------------------ |
| Language        | Python                   |
| Framework       | Streamlit                |
| Data Processing | Pandas, NumPy            |
| Visualization   | Plotly                   |
| Mapping         | Folium                   |
| Map Integration | streamlit-folium         |
| Research ML     | TensorFlow, Scikit-learn |
| Research RL     | OpenAI Gym / DQN         |

---

# ⚙️ Run Locally

## 1. Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_REPOSITORY_NAME>
```

## 2. Create a Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

## 3. Install Dependencies

```bash
pip install streamlit pandas numpy plotly folium streamlit-folium
```

## 4. Run the Application

```bash
streamlit run urbancool_app.py
```

The application will open in your default browser.

---

# 📁 Project Structure

```text
UrbanCool/
│
├── urbancool_app.py
├── README.md
├── requirements.txt
│
└── assets/
    └── screenshots/
```

---

# 🔬 Research & Publication

### Published Research Paper

**AI for Environmental Management: UrbanCool – AI-Driven Responsive Cooling System**

Published in:

**2026 IEEE International Conference for Convergence in Computing Technology (I3CTCON)**

**Publisher:** IEEE

**Paper ID:** 1017

**DOI:**
10.1109/I3CTCON68242.2026.11507747

The paper is available through the **IEEE Xplore Digital Library**.

---

# 👥 Authors

**Paras Chavan**
**Gayatri Kadam**
**Atharv Patil Patki**
**Vaibhav Patil**

### Department

Department of Computer Science and Engineering
PCET's Pimpri Chinchwad University
Pune, India

---

# 🌱 Future Scope

The research proposes several directions for future development:

* 🌫️ Integrated heat and air-quality management
* ☀️ Renewable-energy-powered cooling infrastructure
* ⚡ Edge and cloud computing
* 🌦️ Seasonal climate optimization
* 📡 Real-world IoT sensor deployment
* 🏙️ Large-scale urban deployment
* 📱 Public feedback and comfort monitoring

The long-term goal is to develop UrbanCool toward a real-world, scalable system for intelligent and sustainable urban environmental management.

---

# 📚 Citation

If you reference this research, please cite:

```text
P. Chavan, G. Kadam, A. P. Patki, and V. Patil,
"AI for Environmental Management: UrbanCool – AI-Driven Responsive Cooling System,"
2026 IEEE International Conference for Convergence in Computing Technology (I3CTCON),
2026, doi: 10.1109/I3CTCON68242.2026.11507747.
```

---

## ⭐ Project

UrbanCool demonstrates how artificial intelligence and data-driven decision making can help transform urban cooling from a **reactive process into a predictive and adaptive system**.

### Cooling Smarter. Living Better. ❄️


