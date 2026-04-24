# Miniaturized 2.4 GHz Microstrip Low-Pass Filter Design

This repository contains the design and simulation files for a miniaturized microstrip Low-Pass Filter (LPF) with a cutoff frequency of 2.4 GHz, designed using Ansys Electronics Desktop (HFSS). 

## 📌 Project Overview
The goal of this project was to design a compact LPF suitable for ISM band (2.4 GHz) applications such as Wi-Fi, Bluetooth, and ZigBee. The design focuses on high selectivity and low insertion loss in the passband.

## 🚀 Technical Specifications
| Parameter | Value |
| :--- | :--- |
| Filter Type | Low-Pass (LPF) |
| Cutoff Frequency ($f_c$) | 2.40 GHz |
| Passband Return Loss ($S_{11}$) | > 15 dB |
| Insertion Loss ($S_{21}$) @ $f_c$ | -3.62 dB |
| Stopband Rejection | > 20 dB up to 10 GHz |
| Design Tool | Ansys Electronics Desktop 2024 R2 |

## 📊 Simulation Results

### S-Parameter Analysis
The simulation shows a sharp roll-off after 2.4 GHz with a significant transmission zero near 2.8 GHz, providing excellent out-of-band rejection.

![S-Parameter Plot](images/your_image_name.png) 
*(Note: Replace 'your_image_name.png' with the actual filename in your images folder)*

### Group Delay Analysis
The group delay is remarkably flat within the passband (0 - 2 GHz), ensuring minimal phase distortion for digital signals. A characteristic peak is observed at the cutoff frequency, consistent with high-selectivity filter behavior.

## 📂 File Structure
* /Project_Files: Contains the .aedt project file (Results cleared for size optimization).
* /Images: Contains S-parameter plots and 3D layout screenshots.
* /Docs: (Optional) Datasheet or design equations.

## 🛠 How to Use
1. Clone this repository: git clone https://github.com/your-username/your-repo-name.git
2. Open Ansys Electronics Desktop.
3. Go to File > Open and select the .aedt file.
4. Re-run the simulation to regenerate the mesh and solution data.

## ✍️ Author
Your Name [Your LinkedIn Profile Link
