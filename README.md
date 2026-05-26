# Closed-Loop Digital PI-Controlled Boost Converter Design

## 📌 Project Overview
This repository presents the small-signal modeling, discrete-time frequency-response control design, and transient verification of a high-efficiency DC-DC Boost Converter. Operating a boost converter under closed-loop conditions presents significant control challenges due to its non-minimum phase characteristics and inherent Right-Half Plane (RHP) zero. 

To overcome this, a custom **Python control engine** was developed to linearize the state-space plant dynamics, analyze open-loop stability, and synthesize a well-damped discrete-time PI controller via the Bilinear (Tustin) transform. The physical topology is visually mapped with native vector plotting, completely eliminating the need for restrictive proprietary software interfaces.

---

## 📊 System Design Parameters

| Parameter | Symbol | Design Value |
| :--- | :--- | :--- |
| **Input Voltage** | $V_{in}$ | $12\text{ V}$ |
| **Target Output Voltage** | $V_{out}$ | $24\text{ V}$ |
| **Switching & Sampling Frequency** | $f_{sw}$ / $f_s$ | $100\text{ kHz}$ ($T_s = 10\ \mu\text{s}$) |
| **Power Stage Inductor** | $L$ | $100\ \mu\text{H}$ |
| **Output Filter Capacitor** | $C$ | $47\ \mu\text{F}$ |
| **Nominal Load Resistance** | $R_{load}$ | $12\ \Omega$ |

---

## 📂 Repository Structure
```text
├── notebooks/
│   └── small_signal_analysis.ipynb     # Python discrete tuning & simulation script
├── open_loop_bode.png                  # Linearized plant frequency response plot
├── boost_converter_schematic.png       # Power stage topology & feedback schematic
├── transient_step_response.png         # Closed-loop digital transient tracking plot
└── README.md                           # Main portfolio documentation
