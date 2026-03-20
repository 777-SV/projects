# Laboratory Galvanic Isolation Unit
## Project Overview
### This device is designed for safe diagnostic procedures on high-voltage equipment. It provides complete galvanic isolation from the mains, preventing ground loops and short circuits when using grounded oscilloscopes on "hot" circuits.

<p align="center">
<img src="images/LGIU_main_panel.jpg" width="70%" alt="Isolation Transformer Front Panel" />
</p>

## Technical Architecture
* **Core:** High-efficiency 220V to 220V isolation transformer.

* **Monitoring:** Integrated digital AC multimeter (Voltage, Current, Power, Energy consumption).

* **Chassis:** Custom stainless steel enclosure for durability and EMI shielding.

## Functionality & Controls
The unit is divided into two operational zones with independent logic:

**1. Primary Zone (Direct):**

* 3x Standard AC outlets connected after the power meter but before the transformer.

* Controlled by Red switches.

**2. Isolated Zone (Safety):**

* 2x AC outlets connected to the secondary winding of the isolation transformer.

* Controlled by Yellow switches for visual distinction.

## Safety Features
**Oscilloscope Safety:** Allows for measuring the "hot" side of switching power supplies without the risk of damaging the probe or the mains circuit.

**Soldering Protection:** Provides additional isolation for soldering iron tips, protecting sensitive CMOS components from potential leakage currents.

---

## 📐 3D Design & Interactive Model
To provide a comprehensive view of the mechanical assembly, an interactive 3D PDF is available.

* [**Download 3D Interactive Assembly (PDF)**](documents/LGIU_3D_model.PDF)
    * *Note: Interactive features require Adobe Acrobat Reader. After opening, click "Trust this document" to activate the 3D view.*

<p align="center">
  <img src="images/PDF_preview.png" width="70%" alt="3D Model Preview" />
  <br><em>Visual preview of the internal layout and handle assembly.</em>
</p>

---

## 🛠️ Build Process & Internal Layout
<details>
  <summary><b>Click to expand: Step-by-step Assembly Photos</b></summary>
  <p align="center">
    <img src="images/IMG_1_Bettery.jpg" width="21%" />
    <img src="images/IMG_2_Battery_BMS.jpg" width="37%" />
    <img src="images/IMG_3_Battery_BMS.jpg" width="37%" />
  </p>
  <p align="center">
    <img src="images/IMG_4_Box_USB_charge.jpg" width="61%" />
    <img src="images/IMG_5_Box_Battery.jpg" width="35%" />
  </p>

  <p align="center">
    <img src="images/IMG_6_Led_modules.jpg" width="32%" />
    <img src="images/IMG_7_Led_modules.jpg" width="32%" />
    <img src="images/IMG_8_Led_3D.jpg" width="32%" />
  </p>

  <p align="center">
    <img src="images/IMG_9_Led_Box.jpg" width="48%" />
    <img src="images/IMG_10_Led_Box.jpg" width="48%" />
  </p>
 <p align="center">
    <img src="images/IMG_11_Fuse_Battery.jpg" width="45%" />
    <img src="images/IMG_12_DCDC_modules.jpg" width="25.5%" />
    <img src="images/IMG_13_DCDC_modules.jpg" width="25.5%" />
  </p>
   <p align="center">
    <img src="images/IMG_14_Box_DCDC_ports.jpg" width="45%" />
    <img src="images/IMG_15_Box_Battery_montag.jpg" width="25.5%" />
    <img src="images/IMG_16_Box_Battery_montag.jpg" width="25.5%" />
  </p>
  <p align="center">
    <img src="images/IMG_17_Power_B_Panel.jpg" width="32%" />
    <img src="images/IMG_Power_B_panel.jpg" width="32%" />
    <img src="images/IMG_flashlight_handle.jpg" width="32%" />
  </p>
  <p>
    <b>Engineering Note:</b> During the assembly, special attention was paid to wire management and insulation. 
    I used a <b>Daly Active Balancer</b> alongside the BMS to ensure long-term cell health. 
    All high-current paths are reinforced and fused for maximum safety.
  </p>
</details>



