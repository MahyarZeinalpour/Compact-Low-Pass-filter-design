# Compact Microstrip Low Pass Filter — 2.4 GHz Cutoff Frequncy

Simulated in Ansys HFSS 2024 R2 | Rogers RO4003 | L-Shaped Resonators

---

## Overview

This repository presents the design and full-wave EM simulation of a compact microstrip low pass filter (LPF) targeting the 2.4 GHz ISM band. The filter is implemented on a Rogers RO4003 substrate and employs a combination of lower-L and upper-L shaped resonators to achieve a sharp roll-off, deep transmission null at the passband edge, and wideband stopband suppression up to 10 GHz.

The design was developed and simulated using Ansys HFSS 2024 R2 (Driven Modal solution type) and has been fully validated through adaptive mesh convergence across three consecutive passes.

---

## Key Specifications

| Parameter | Value |
|---|---|
| Substrate | Rogers RO4003 |
| Substrate thickness | 1.15 mm |
| Dielectric loss tangent | 0.0021 |
| Filter dimensions | 34.5 × 15 mm |
| −3 dB cutoff frequency | ≈ 2.40 GHz |
| Return loss (passband) | < −20 dB |
| Transmission null depth | < −40 dB (at ≈ 2.4 GHz) |
| Stopband suppression (to 10 GHz) | > 20 dB |
| Group delay (passband) | ≈ 0.4 ns (flat) |
| Convergence (Max Mag. ΔS) | 0.0054433 (target: 0.01) |
| Simulation passes | 22 of 60 maximum |

---

## Filter Topology

The filter uses two types of resonator structures:

- Lower-L shaped resonators — Introduce a sharp transmission null near the cutoff frequency (≈ 2.4 GHz), enabling a fast roll-off from passband to stopband.
- Upper-L shaped resonators — Suppress high-frequency spurious responses that appear in the initial design between 8–10 GHz, extending clean stopband rejection to 10 GHz.

---

## Simulation Results

### Initial Design
- fc ≈ 2.40 GHz
- S11 < −20 dB in passband
- Transmission null below −37 dB at ≈ 2.4 GHz
- Spurious response observed between 8–10 GHz

### Improved Design
- fc ≈ 2.40 GHz (cursor confirmed: S11 ≈ −3.81 dB, S21 ≈ −2.98 dB)
- S11 < −20 dB across the full passband
- Transmission null below −40 dB at ≈ 2.4 GHz
- Stopband suppression > 25 dB maintained up to 10 GHz
- Minor resonances near 6 GHz remain below −20 dB

### Group Delay
Nearly flat at ≈ 0.4 ns across the passband (0–2.4 GHz), confirming minimal phase distortion.

---

## Repository Structure
compact-LPF-2.4GHz/
├── HFSS file-compact Low Pass Filter
│   
├── Results/
│   ├── S_parameters_initial.png
│   ├── S_parameters_improved.png
│   ├── Group_delay.png
│   ├── Convergence_plot.png
│   ├── E_field_initial.png
│   └── E_field_improved.png
├── Report/
│   └── low_pass_filter_report.pdf
└── README.md

---

## Simulation Environment

| Tool | Version |
|---|---|
| Ansys HFSS | 2024 R2 |
| Solution type | Driven Modal |
| Meshing | Adaptive |
| Convergence target | Max Mag. ΔS < 0.01 |
| Consecutive passes required | 3 |

---

## Applications

- ISM band (2.4 GHz) RF front-end filtering
- Wi-Fi / Bluetooth harmonic suppression
- Space-constrained portable and mobile RF systems

---

## Author

Mahyar Zeinalpour  
RF & Microwave Engineer  
MSc Telecommunications Engineering — Politecnico di Torino

---

## License

This project is shared for educational and research reference purposes.  
Please cite or credit appropriately if used in academic or professional work.
