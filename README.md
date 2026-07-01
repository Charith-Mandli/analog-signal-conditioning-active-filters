# Active Analog Filter Design and Analysis using LTspice

## Overview

This project presents the design, simulation, and comparative analysis of **first-order** and **second-order active filters** for analog signal conditioning using **LTspice**.

The work investigates the frequency-selective behaviour of active **Low-Pass (LPF)** and **High-Pass (HPF)** filters by comparing different filter orders while maintaining a common cutoff frequency of approximately **1 kHz**.

The circuits were designed using operational amplifier-based topologies, validated through **AC Sweep** and **Transient** simulations, and further analyzed by varying passive component values to study the influence of the RC time constant on filter characteristics.

---

## Project Objectives

- Design first-order active LPF and HPF circuits
- Design second-order Sallen-Key LPF and HPF circuits
- Validate theoretical cutoff frequency using LTspice
- Compare first-order and second-order frequency responses
- Analyze attenuation and phase characteristics
- Investigate component variation effects on cutoff frequency
- Develop practical understanding of analog signal conditioning

---

## Design Specifications

| Parameter | Value |
|-----------|--------:|
| Simulation Software | LTspice XVII |
| Operational Amplifier | UniversalOpamp2 |
| Supply Voltage | ±15 V |
| Design Cutoff Frequency | ≈ 1 kHz |
| Resistor Value | 15.9 kΩ |
| Capacitor Value | 10 nF |

---

## Active Filter Topologies

The following active filter configurations were implemented and analyzed.

| Filter | Topology |
|----------|----------------------|
| First-Order Low-Pass Filter | RC Network + Voltage Follower |
| First-Order High-Pass Filter | RC Network + Voltage Follower |
| Second-Order Low-Pass Filter | Unity-Gain Sallen-Key |
| Second-Order High-Pass Filter | Unity-Gain Sallen-Key |

---

## Working Principle

The filters selectively process signals based on frequency.

```text
          Input Signal
               │
               ▼
     Active Filter Circuit
               │
     ┌─────────┴─────────┐
     │                   │
 Low Frequency      High Frequency
 Components          Components
     │                   │
     ▼                   ▼
 LPF Passes         HPF Passes
```

The cutoff frequency for all filter configurations is given by

<img width="185" height="85" alt="Formula 1" src="https://github.com/user-attachments/assets/55abea92-08c3-459e-b45a-63d7bbc2bb3f" />

Using

- R = 15.9 kΩ
- C = 10 nF

results in

**Cutoff Frequency ≈ 1 kHz**

---

## Project Structure

```text
Active-Filter-Signal-Conditioning/
│
├── calculations/
│   └── Design_Calculations.pdf
│
├── docs/
│   └── Project_Report.pdf
│
├── images/
│   ├── schematics/
│   ├── ac_sweeps/
│   ├── transient/
│   └── component_variation/
│
├── ltspice/
│   ├── first_order_lpf.asc
│   ├── first_order_hpf.asc
│   ├── second_order_lpf.asc
│   └── second_order_hpf.asc
│
├── README.md
├── LICENSE
└── .gitignore
```

---

## Repository Contents

| Folder | Description |
|----------|-------------|
| calculations | Design calculations and cutoff frequency derivations |
| docs | Complete project report |
| images | Circuit schematics and simulation screenshots |
| ltspice | LTspice schematic files (.asc) |
| README.md | Project documentation |
| LICENSE | Open-source license |

---

## Design Verification

The designed circuits were evaluated using multiple simulation scenarios.

### Simulations Performed

- AC Sweep Analysis
- Transient Analysis
- Cutoff Frequency Verification
- Phase Response Analysis
- Component Variation Analysis
- First vs Second Order Comparison
- Low-Pass vs High-Pass Comparison

---

## Simulation Results

### 1. Filter Implementations

<img width="1599" height="899" alt="filter_topologies" src="https://github.com/user-attachments/assets/bf5ef022-61d2-432f-8b26-5696b8b0d03b" />

---

### 2. Component(Resistance) Variation Analysis

<img width="2420" height="1430" alt="AC_LPF_Resistor_Comparison" src="https://github.com/user-attachments/assets/8b127a05-98df-41d3-ba27-e6ce10c5623f" />

---

### 3. Component(Capacitance) Variation Analysis

<img width="2420" height="1430" alt="AC_HPF_Capacitor_Comparison" src="https://github.com/user-attachments/assets/ba05eeef-b47d-4957-b473-ad7f7a7d2ee7" />

---

### 4. LPF Transient Response

<img width="1902" height="417" alt="transient_1kHz" src="https://github.com/user-attachments/assets/9b2ab573-d7db-4adc-a1bf-1c7746d96425" />


---

### 5. HPF Transient Response

<img width="1905" height="425" alt="transient_1kHz" src="https://github.com/user-attachments/assets/97be76f0-8495-43a2-974d-b0cb0166bde1" />

---

## Key Observations

- Simulated cutoff frequencies closely matched theoretical calculations.
- First-order filters exhibited approximately **20 dB/decade** attenuation beyond the cutoff frequency.
- Second-order Sallen-Key filters achieved approximately **40 dB/decade** attenuation, demonstrating improved frequency selectivity.
- Low-pass and high-pass filters exhibited complementary frequency-selective behaviour.
- Varying resistor or capacitor values shifted the cutoff frequency while preserving the overall filter characteristics.

---

## Implementation Notes

During circuit development, the choice of operational amplifier model and proper supply configuration significantly influenced the simulation results.

The final implementation was standardized using **UniversalOpamp2** powered from **±15 V**, ensuring stable operation and agreement with theoretical filter responses. This highlighted the practical importance of appropriate op-amp selection and power supply configuration in simulation-driven analog circuit design.

---

## Tools Used

- LTspice XVII
- Analog Filter Theory
- Operational Amplifier Fundamentals

---

## Key Learnings

- Active analog filter design
- First-order and second-order filter implementation
- Sallen-Key topology
- Frequency response analysis
- Bode plot interpretation
- AC Sweep and Transient simulation
- Component selection based on cutoff frequency
- Simulation-based circuit verification using LTspice

---

## Future Improvements

- Design higher-order active filters
- Compare Butterworth, Bessel and Chebyshev responses
- Implement tunable active filters
- Validate simulation results using hardware implementation
- Evaluate practical op-amp bandwidth limitations

---

## References

- Sedra & Smith — *Microelectronic Circuits*
- Sergio Franco — *Design with Operational Amplifiers and Analog Integrated Circuits*
- Analog Devices — LTspice Documentation

---

## Author

**M. V. S. Charith**
