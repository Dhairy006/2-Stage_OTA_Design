# Two-Stage OTA Design Using TSMC 180nm Technology

![License](https://img.shields.io/badge/Project-Academic-blue)
![Technology](https://img.shields.io/badge/Technology-TSMC%20180nm-green)
![Tool](https://img.shields.io/badge/Simulation-LTspice-orange)

## Overview

This project presents the complete design, theoretical analysis, transistor sizing, frequency compensation, and simulation verification of a **Two-Stage Operational Transconductance Amplifier (OTA)** implemented using **TSMC 180nm CMOS technology**.

The objective was to design a stable, high-gain OTA satisfying gain, bandwidth, phase margin, and transient response requirements through both analytical calculations and LTspice simulations.

The project includes:

- Manual hand calculations
- Transistor sizing using square-law MOSFET equations
- Small-signal analysis
- Frequency compensation design
- Open-loop AC analysis
- Closed-loop transient analysis
- Validation using LTspice and BSIM device models

---

## Design Specifications

| Parameter | Value |
|------------|---------|
| Technology | TSMC 180nm CMOS |
| Supply Voltage | 1.8 V |
| Compensation Capacitor (Cc) | 2.5 pF |
| Nulling Resistor (Rz) | 500 Ω |
| Load Capacitor (CL) | 5 pF |
| Architecture | Two-Stage OTA |

---

## OTA Architecture

The amplifier consists of:

### First Stage
- Differential NMOS input pair
- PMOS current mirror active load
- Provides high differential gain

### Second Stage
- Common-source gain stage
- Enhances overall voltage gain

### Compensation Network
- Miller Compensation Capacitor (Cc)
- Nulling Resistor (Rz)
- Improves stability and phase margin

---

## Design Methodology

### 1. Hand Calculations

Theoretical calculations include:

- Current budgeting
- Overdrive voltage selection
- MOSFET sizing (W/L)
- Transconductance (gm)
- Output resistance (ro)
- Open-loop gain estimation
- Pole-zero analysis
- Frequency compensation
- Power dissipation estimation

### 2. Circuit Implementation

The designed OTA was implemented in LTspice using:

- TSMC 180nm BSIM models
- Calculated transistor dimensions
- Compensation components

### 3. Verification

The design was validated through:

- DC Operating Point Analysis
- AC Frequency Response Analysis
- Closed-Loop Step Response Analysis

---

## Simulation Results

### DC Operating Point

Selected operating-point results obtained from LTspice:

| Device | ID | gm | ro |
|----------|----------|----------|----------|
| M0 | 67.05 µA | 670.5 µS | 149.1 kΩ |
| M1, M2 | 33.52 µA | 335.2 µS | 298.3 kΩ |
| M3, M4 | 33.52 µA | 335.2 µS | 298.3 kΩ |
| M5 | 195.59 µA | 1955.9 µS | 51.1 kΩ |
| M6 | 195.59 µA | 1955.9 µS | 51.1 kΩ |
| M7 | 8.00 µA | 80.0 µS | 1.25 MΩ |

---

### Open-Loop Performance

| Metric | Simulated Value |
|----------|----------|
| DC Gain | 67.16 dB |
| Linear Gain | ≈ 2300 V/V |
| Phase Margin | 58.39° |
| Unity Gain Frequency | 20.04 MHz |
| Unity Gain Angular Frequency | 125.91 Mrad/s |

### Performance Assessment

✅ Gain requirement satisfied

✅ Stable frequency response

✅ Adequate phase margin

✅ Proper compensation achieved

---

### Closed-Loop Performance

Configuration:

- Non-inverting amplifier
- Closed-loop gain = 2 V/V
- Input step = 0.2 V

Results:

| Parameter | Value |
|------------|---------|
| Input Step | 0.2 V |
| Expected Output Step | 0.4 V |
| Settled Voltage | 1.2995 V |
| Peak Voltage | 1.380 V |

The transient response confirms:

- Stable operation
- Fast settling
- Accurate gain realization
- Controlled overshoot

---

## Project Structure

```text
2-Stage_OTA_Design/
│
├── EE_206_DesignOTA_2262.pdf
├── README.md
│
└── Figures
    ├── Hand Calculations
    ├── Circuit Schematics
    ├── AC Response
    └── Transient Response
```

---

## Key Concepts Demonstrated

- Analog CMOS IC Design
- Differential Amplifiers
- Current Mirrors
- Operational Transconductance Amplifiers
- Small-Signal Modeling
- Frequency Compensation
- Pole-Zero Cancellation
- Stability Analysis
- Phase Margin Optimization
- LTspice Simulation

---

## Tools Used

- **LTspice**
- **TSMC 180nm CMOS Models**
- **Analog CMOS Design Theory**
- **Small-Signal Analysis Techniques**

---

## Results Summary

| Metric | Achieved |
|----------|----------|
| Open-Loop Gain | 67.16 dB |
| Phase Margin | 58.39° |
| Unity Gain Frequency | 20.04 MHz |
| Closed-Loop Gain | 2 V/V |
| Stable Operation | Yes |
| Compensation Verified | Yes |

---

## Report

The complete derivation, calculations, schematics, and simulation results can be found in:

**`EE_206_DesignOTA_2262.pdf`**

---

## Author

**Dhairya Shivhare**  
Roll Number: 240102262  
Department of Electronics and Electrical Engineering  
Indian Institute of Technology Guwahati (IIT Guwahati)

---

## Acknowledgements

This project was completed as part of an Analog Integrated Circuit Design assignment involving the design and verification of a compensated Two-Stage Operational Transconductance Amplifier using CMOS technology.

---
