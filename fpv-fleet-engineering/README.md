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
* **[Power Reliability (Capacitor Reinforcement):](images/reinforced_capacitor_leads_2.jpg)** To prevent lead fatigue and failure under high ESR stress, I implemented a **double-fold and pre-tinning technique** for capacitor leads. This increased the conductor cross-section and mechanical structural integrity.
* **[Custom 3D Printed Optics (TPU D100):](images/tpu_camera_mount_fixed_1.jpg)** Designed and manufactured custom camera mounts using **D100 Elastane**.
    * *Result:* Superior vibration damping (jello reduction), forward-shifted FOV to minimize propeller interference, and improved tilt-angle adjustability.
* **[Electrical Isolation:](images/vtx_insulation_layer_2.jpg)** Utilized **self-adhesive electrical grade pressboard (Fish paper)** to isolate high-power VTX modules from the conductive carbon fiber frame, preventing shorts and interference.
* **Hardware Debugging:** Diagnosed and rectified manufacturing defects, including incorrect ribbon cable pinouts that contradicted official documentation.
* **Payload Systems & Servo Integration (Power & Logic):**
    * **Challenge:** Integrating multiple high-torque servos for drop systems on 10" frames caused two major issues: **5V rail brownouts** (due to high peak current draw) and **firmware resource conflicts** (limited PWM mapping in standard Betaflight targets).
    * **Solution:** * **Power:** Bypassed the flight controller's internal BEC by implementing **dedicated external DC-DC Buck converters**. This isolated the servos' "dirty" power from the sensitive flight electronics, preventing mid-air reboots.
        * **Logic:** Re-mapped unused Motor/LED pads via CLI to create additional PWM outputs and overcame firmware limitations by custom-assigning resources to handle multiple payload triggers simultaneously.
---

## 5. Quality Control (QC) Protocol
Every unit underwent a rigorous multi-stage verification process before deployment:

1.  **Smoke Stopper Test:** Initial power-up via current-limiting protection to prevent catastrophic failure.
2.  **Visual & Mechanical Inspection:** Audit of solder joint integrity, wire management, and structural rigidity.
3.  **Bench Testing:** Sensor calibration, motor vibration analysis, and VTX power output verification.
4.  **Range Test:** Validation of RC link and video feed quality under low-power conditions to ensure operational range.

##  Build Process & Internal Layout
<details>
 <summary><b>📦 Sourced Components & Hardware Selection</b></summary>
  <p align="center">
    <img src="images/component_selection_kit_1.jpg" width="48%" />   
    <img src="images/VTX_AKK_1.jpg" width="48%" />  
  </p>  
   <p align="center">
    <img src="images/VTX_GepRC_1.jpg" width="48%" />   
    <img src="images/VTX_MAXSOLO_1.jpg" width="48%" />  
  </p> 
   <p align="center">
    <img src="images/tpu_camera_mount_fixed_1.jpg" width="32%" />
    <img src="images/tpu_camera_mount_fixed_2.jpg" width="32%" />
    <img src="images/tpu_camera_mount_fixed_3.jpg" width="32%" />
  </p>
   <p align="center">
    <img src="images/tpu_camera_mount_fixed_1.jpg" width="32%" />
    <img src="images/tpu_camera_mount_fixed_2.jpg" width="32%" />
    <img src="images/tpu_camera_mount_fixed_3.jpg" width="32%" />
  </p>
</details>
<details>
  <summary><b>🔋 Battery Pack Assembly (Spot Welding & Geometry)</b></summary>
  <p align="center">
    <img src="images/molicel_p42a_inventory.jpg" width="32%" />
    <img src="images/busbar_geometry_test_1.jpg" width="32%" />
    <img src="images/busbar_geometry_test_2.jpg" width="32%" />
  </p>
   <p align="center">
    <img src="images/custom_3d_printed_spacers_1.jpg" width="42%" />
    <img src="images/custom_3d_printed_spacers_2.jpg" width="42%" />   
  </p>
   <p align="center">
    <img src="images/final_battery_packs_testing.jpg" width="90%" />      
  </p>
</details>

<details>
  <summary><b>🛠️ Drone Assembly & Hardware Modifications</b></summary>
  <p align="center">
    <img src="images/stack_wiring_clean.jpg" width="32%" />
    <img src="images/capacitor_reinforcement.jpg" width="32%" />
    <img src="images/camera_mount_tpu_d100.jpg" width="32%" />
  </p>
  <p align="center">
    <img src="images/vtx_insulation_layer.jpg" width="48%" />
    <img src="images/external_bec_integration.jpg" width="48%" />
  </p>
</details>

<details>
  <summary><b>🚁 Completed Builds & Quality Control Testing</b></summary>
  <p align="center">
    <img src="images/fleet_overview_7to8_1.jpg" width="32%" />
    <img src="images/fleet_overview_7to8_2.jpg" width="32%" />
     <img src="images/fleet_overview_7to8_3.jpg" width="32%" />
  </p>
  <p align="center">
    <img src="images/fpv_7inch_APEX_1.jpg" width="32%" />
    <img src="images/fpv_7inch_APEX_2.jpg" width="32%" />
    <img src="images/fpv_7inch_APEX_3.jpg" width="32%" />
  </p>
    <p align="center">
    <img src="images/fpv_7inch_strike_build_2.jpg" width="32%" />
    <img src="images/fpv_7inch_strike_build_1.jpg" width="32%" />
    <img src="images/fpv_7inch_strike_build_3.jpg.jpg" width="32%" />
  </p>
    </p>
    <p align="center">
    <img src="images/fpv_9inch_1.jpg" width="43%" />
    <img src="images/fpv_9inch_2.jpg" width="43%" />
     </p>
</details>
