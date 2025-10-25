# Instrumentation Amplifiers for Measurement of EMG Signals

## Overview
This project focuses on designing and building an **Instrumentation Amplifier Circuit** specifically for measuring **Electromyography (EMG)** signals.  
The EMG signal is a bioelectrical signal produced by skeletal muscles, generally spanning **0.1 mV–5 mV** in amplitude and occupying a frequency range of **0–500 Hz**.  
To accurately capture and amplify this low-frequency, low-amplitude signal, the circuit design integrates both **high CMRR instrumentation amplification** and **selective bandpass filtering**, ensuring minimal noise interference and maximum fidelity.

---

## Objectives
- To design a **low-noise instrumentation amplifier** for biomedical EMG signal acquisition.  
- To achieve optimal **common-mode noise rejection** and **signal integrity**.  
- To implement a **bandpass filter** that passes frequencies relevant to EMG (50–150 Hz).  
- To validate the design using circuit simulations and performance testing.

---

## Project Architecture
The system is divided into two core functional blocks:

### 1. Instrumentation Amplifier Block
- Built using a **three-op-amp configuration** based on **OP07** operational amplifiers.  
- Provides high input impedance, excellent stability, and precise gain control.  
- Achieves an experimental gain of approximately **54 V/V**, aligning closely with the expected **55 V/V** value.  
- Ensures **high CMRR**, effectively filtering out common-mode interference and power-line noise.

### 2. Bandpass Filter Block
- Implements a **6th-order active bandpass filter** with a passband between **50 Hz and 250 Hz**.  
- Designed to preserve the EMG signal energy (primarily in 50–150 Hz) while blocking unwanted components.  
- Demonstrated strong attenuation of frequencies at **20 Hz** and **1 kHz**, confirming the filter’s effective roll-off characteristics.

---

## Circuit Design and Components
The project employs through-hole components, structured using **KiCad PCB Design Tools**.

### Key Components
- **ICs:** OP07 (x7)  
- **Resistors:** Ranging between 1 kΩ to 680 kΩ  
- **Capacitors:** 2.2 nF to 10 µF (radial THT)  
- **Connectors:** 2.54 mm pitch sockets for input/output  
- **Power Supply:** ±12 V DC dual supply  

### Tools Used
- **Simulation:** Tektronix TBS1072B Digital Oscilloscope  
- **PCB Design:** KiCad (schematic capture, footprint assignment, ERC, DRC)  
- **3D Visualization:** KiCad 3D Model View  

---

## Results and Testing

### Instrumentation Amplifier Testing:
- **Input:** 2 mV (differential, 180° out of phase)  
- **Output:** 216 mV  
- **Gain:** ~54 V/V (validated via oscilloscope readings)

### Filter Testing:
- **Input:** 100 mV sine wave at various frequencies  
- **20 Hz →** Output attenuated heavily  
- **100 Hz →** Signal passed cleanly  
- **1 kHz →** Output significantly reduced  

This confirms the amplifier–filter chain delivers the desired selective response and accuracy for EMG signal acquisition.

---

## PCB Design
The PCB was designed for compactness and low interference:

- **Schematic Capture:** Completed with correct symbol–footprint mapping  
- **Electrical Rule Check (ERC):** No major unconnected items or design violations  
- **Design Rule Check (DRC):** Verified compliance with layout standards  
- **3D View:** Ensured precise component placement for manufacturing  

---

## Applications
- Biomedical instrumentation, specifically **EMG signal measurement**  
- Medical research and muscle activity analysis  
- Biosignal processing and human–machine interface systems  
- Educational projects for analog circuit design and bioelectronics  
