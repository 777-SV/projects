# 🔊 JLH2005 Class-A Amplifier Implementation & Optimization

## 1. Project Overview
This project presents a highly optimized, custom implementation of the classic **John Linsley-Hood (JLH2005) Class-A amplifier**. Known for its exceptional acoustic transparency, the circuit has been redesigned to improve thermal management, power supply ripple rejection, and overall operational reliability.

* **Status:** PCB designed, manufactured, and populated; mechanical chassis design in progress (CAD stage).
* **Core Focus:** Ultra-low noise floor, robust power delivery, and switchable bias states.

---

## 2. Technical Architecture & Modifications
To overcome the inherent limitations of standard Class-A designs (high heat dissipation and sensitivity to PSU ripple), the following engineering upgrades were analyzed and integrated:

### ⚡ Power Supply Integrity (PSU)
* **High-Capacity Transformer:** Sourced with a substantial power headroom to prevent core saturation under continuous Class-A current load.
* **Dual-Rail CRC Filtering:** Implemented dedicated **CRC (Capacitor-Resistor-Capacitor) filters** in each voltage rail to suppress high-frequency rectifying noise.
* **Electronic Choke (Capacitance Multiplier):** Integrated an active transistor-based ripple filter (electronic choke) to achieve an extremely low noise floor, critical for high-sensitivity acoustic systems.

### 🎛️ Circuit Optimizations & Bias Control
* **Relay-Controlled Dual Bias Modes:** Designed a circuit utilizing mechanical relays to switch between **two pre-set quiescent current (Id) levels**. This allows for a "Power Save/Warm-up" mode and a "Full Performance" mode, optimizing thermal output when maximum power is not required.
* **Component Selection:** Upgraded critical feedback loops and signal path coupling with audiophile-grade, tight-tolerance components.

---

## 3. PCB Design & Manufacturing
* **Routing Strategy:** Custom PCB layout designed from scratch. Special attention was paid to heavy-current paths (ground planes, power rails) to minimize stray inductance and resistance.
* **Signal Isolation:** Separated low-level audio input ground from the high-current power ground (Star Grounding topology) to eliminate ground loops.
* **Manufacturing:** Fabricated via industrial PCB manufacturing processes (FR-4, thick copper layer, solder mask, and silk-screening).

---

## 4. Current Stage: Mechanical & Enclosure Design
The project is currently transitioning into the **Enclosure Design phase** using SolidWorks. 
* **Key Challenges:** Calculating the required surface area of aluminum heatsinks to dissipate continuous thermal load from the Class-A output stage without exceeding $65^\circ\text{C}$ on the chassis.
