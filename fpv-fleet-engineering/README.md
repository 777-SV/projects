# 🛸 FPV Fleet Deployment & Custom Engineering (7" - 10")

## 1. Introduction
This project was executed as part of the **Social Drone UA** volunteer initiative. The primary objective was the rapid assembly, precision tuning, and deployment of reliable UAV solutions for specialized field operations.

* **Scale:** Successfully assembled and configured **11+ UAV units**.
* **Project Specifics:** Unlike ready-to-fly kits, every unit was built from individually sourced components, requiring deep technical analysis of hardware compatibility and market availability.

---

## 2. Technical Stack
Component selection was based on a balance of reliability, performance, and mission-specific requirements:

* **Frames & Motors:** A versatile range from **7"** (high-speed interceptors) to **10"** (heavy-lift platforms for relay and drop systems).
* **Flight Stacks:** Primarily utilized **SpeedyBee F405 (50A/55A)** — selected as the industry standard for flight stability and durability.
* **Video Systems (VTX):** Integration of high-power transmitters including **AKK, Foxeer, and Rush Tank Solo**, optimized for long-range signal penetration.
* **RC Link (ELRS):** Expert implementation of **915MHz** and **2.4GHz** links. Expertise in antenna physics and custom firmware flashing to enhance resilience against Electronic Warfare (EW).

---

## 3. Firmware & Configuration
* **Betaflight:** Comprehensive software initialization, advanced notch filtering, and **PID tuning**.
* **ArduPilot:** Implementation of systems for autonomous missions and waypoint navigation (current area of R&D).
* **Custom RX/TX:** Deployment of firmware supporting **Frequency Hopping** to significantly increase link survivability in contested environments.

---

## 4. Engineering "Napylok" Solutions (Hardware Optimization)
Since all components were sourced separately, I encountered numerous technical challenges that required custom engineering workarounds:

* **Vibration Management:** Modified mounting points on 7" frames with rigid stack fixtures to integrate **soft-mounting dampers**. This eliminated high-frequency oscillations and allowed for cleaner gyro data.
* **Power Reliability (Capacitor Reinforcement):** To prevent lead fatigue and failure under high ESR stress, I implemented a **double-fold and pre-tinning technique** for capacitor leads. This increased the conductor cross-section and mechanical structural integrity.
* **Custom 3D Printed Optics (TPU D100):** Designed and manufactured custom camera mounts using **D100 Elastane**.
    * *Result:* Superior vibration damping (jello reduction), forward-shifted FOV to minimize propeller interference, and improved tilt-angle adjustability.
* **Electrical Isolation:** Utilized **self-adhesive electrical grade pressboard (Fish paper)** to isolate high-power VTX modules from the conductive carbon fiber frame, preventing shorts and interference.
* **Hardware Debugging:** Diagnosed and rectified manufacturing defects, including incorrect ribbon cable pinouts that contradicted official documentation.

---

## 5. Quality Control (QC) Protocol
Every unit underwent a rigorous multi-stage verification process before deployment:

1.  **Smoke Stopper Test:** Initial power-up via current-limiting protection to prevent catastrophic failure.
2.  **Visual & Mechanical Inspection:** Audit of solder joint integrity, wire management, and structural rigidity.
3.  **Bench Testing:** Sensor calibration, motor vibration analysis, and VTX power output verification.
4.  **Range Test:** Validation of RC link and video feed quality under low-power conditions to ensure operational range.
