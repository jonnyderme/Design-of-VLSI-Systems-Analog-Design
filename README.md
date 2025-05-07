# Design-of-VLSI-Systems-Analog-Design
Assignments for the "Design of VLSI Systems/Analog Design" Course Faculty of Engineering, AUTh School of Electrical and Computer Engineering: Operational Transcondunce Amplifier and Memristors 


# ⚙️ VLSI Systems Design – Computational Assignment (2024)

📚 **Course:** Design of VLSI Systems / Analog Design  
🏛️ **Faculty:** AUTh – School of Electrical and Computer Engineering  
📅 **Semester:** 9th Semester, 2023–2024  
👥 **Team 12:**  

---

## 📝 Project Overview

This project focuses on the **design, simulation, and layout** of a **Telescopic Operational Transconductance Amplifier (OTA)** using the **Cadence Virtuoso** platform. The goal is to evaluate the analog performance of the OTA in both schematic and post-layout levels under 180nm CMOS technology constraints.

---

## 🧠 Theoretical Background

A **Telescopic OTA** is a high-gain, low-power analog amplifier commonly used in signal processing, filters, and ADCs. It operates as a **VCCS** (Voltage-Controlled Current Source), where the output current is linearly proportional to the input differential voltage.

### ⚙️ Structure and Operation

The amplifier consists of:

- **PMOS differential pair** at the input for better matching and low flicker noise.
- **Current mirrors** for biasing and active loading.
- **Cascode transistors** for gain enhancement (stacked above input transistors).
- **High output resistance (r<sub>out</sub>)** and moderate transconductance (g<sub>m</sub>), achieving a high gain:
  
  \[
  A_v = g_m \cdot r_{out}
  \]

- Bias voltages ensure the transistors remain in saturation, while output swing is bounded by stacked devices.

### ✨ Advantages

- ✅ High intrinsic gain  
- ✅ Low power consumption  
- ✅ Good frequency performance  
- ✅ Small area layout

### ⚠️ Limitations

- ❗ Limited output swing (due to stacking of devices)  
- ❗ Narrow common-mode input range  
- ❗ Less flexibility compared to folded cascode topologies

### 📈 Performance Metrics

| Metric              | Description                                      |
|---------------------|--------------------------------------------------|
| DC Gain             | Ratio of output to input voltage (in dB)         |
| Phase Margin        | Indicator of system stability                    |
| GBW Product         | Determines speed-performance tradeoff            |
| Output Swing        | Max achievable voltage range at the output       |
| Slew Rate           | How fast output responds to input change         |
| DRC / LVS           | Verification of physical and electrical validity |

---

## 🔬 Tools Used

- 🛠 **Cadence Virtuoso** — Design entry and circuit layout  
- 📐 **PVS (DRC/LVS)** — Design rule and layout vs. schematic checks  
- 📊 **Spectre Simulator** — AC, DC, and transient response analysis  

---

## 📈 Key Results

- **DC Gain:** 44.97 dB  
- **Phase Margin:** 88.39°  
- **Bandwidth:** ~509.2 kHz  
- **GBW Product:** 16.83 MHz  
- **Output swing:** 177.15 mV  
- **DRC & LVS:** ✅ Passed  

---

## 📚 References

1. Jamuna G. & Siva S. Yellampalli – *Design and Analysis of CMOS Telescopic OTA for 180nm Technology*  
2. Kush Gulati & Hae-Seung Lee – *A High-Swing CMOS Telescopic Operational Amplifier*  
3. Sarin V. Mythry et al. – *High Gain CMOS Telescopic OTA in 180nm for Biomedical & RF Applications*

---

## ✅ Verification Summary

| Check Type | Status     |
|------------|------------|
| DRC        | ✔️ Passed |
| LVS        | ✔️ Passed |
| Specs Met  | ✔️ Fully  |

---
---
# ⚙️ Design of VLSI Systems – Bibliographical Assignment  
---

## 🧠 Project Title: Memristors – Theory, Simulation, and Applications
---

## 📚 Overview  

This project explores **memristors**, the fourth fundamental passive circuit element, following resistors, capacitors, and inductors. Introduced theoretically in 1971 by Leon Chua and practically realized in 2008, memristors provide a direct relationship between electric charge and magnetic flux. Their memory-dependent resistance allows for numerous applications in analog computing, logic design, and non-volatile memory systems.

---

## 🔬 Key Topics Explored

### 📌 1. Fundamentals of Memristors  
- Behavior and definition of **memristance**  
- V–I characteristic under varying frequency  
- Types: Metal-oxide (TiO₂), Polymer/Ionic, Manganite-based

### 📌 2. CMOS Memristor Emulator  
- Implemented in 90nm CMOS  
- Consists of 3 NMOS transistors + 1 capacitor  
- Time-dependent resistance simulating memristive behavior  
- Non-volatile memory emulation

### 📌 3. Applications  
#### 🔁 A. BFSK Modulator/Demodulator  
- Frequency-shift keyed logic for data encoding  
- Detection using memristor’s frequency-sensitive resistance  

#### 🧮 B. Memristive Logic Gates  
- AND / OR / XOR gate design using resistance states  
- Logic behavior via current direction and polarity  

#### 💾 C. ReRAM Systems  
- Crossbar arrays with 1T1R and 2T1R memory cell primitives  
- Dense memory with programmable memristors  
- Integration with CMOS and analog acceleration  

#### 🧠 D. Edge Detection  
- Crossbar memristor arrays for image processing  
- 8×8 binary pattern logic for pixel comparison  

### 📌 4. Lifetime & Aging  
- Resistance drift over time (RON/ROFF degradation)  
- Methods: pulse regulation, write minimization, reuse protocols

### 📌 5. Ternary Logic Systems  
- Support for 3-state logic (LOW, MID, HIGH)  
- Implementation of gates and inverters (TAND, STI, PTI, NTI)  
- Memristor-based circuits for compact multi-valued logic

---

## 📄 References  
The report includes references to recent IEEE papers discussing the implementation, layout, and functionality of memristor-CMOS hybrid circuits, aging behavior, and advanced ternary logic systems.

---

## 📁 Repository Structure

```
📁 Repository Structure

├── README.md                          # Project overview for both assignments

├── VLSI_Analog_Design/                # Computational assignment directory
│   ├── OTA/                           
│   │   └── lab_report_team12.pdf      # Detailed report including schematic, layout, and simulations
│   │   └── References.txt             # Key papers cited in the project
│
│   └── References.txt                 # (Optional) duplicate if outside OTA folder
│       └── [1] Jamuna G. and Siva S. Yellampalli, “Design and Analysis of CMOS Telescopic OTA”
│       └── [2] Kush Gulati and Hae-Seung Lee, “A High-Swing CMOS Telescopic OTA”
│       └── [3] Sarin V. Mythry et al., “Design and Analysis of High Gain CMOS Telescopic OTA...”

├── Bibliographical Assignment/        # Bibliographical research on Memristors
│   ├── Literature Review/             
│   │   └── lit_review_team12.pdf      # Final literature report (Memristors)
│
│   ├── Sources/                       # Cited papers and additional resources
│
│   ├── Presentation/                 
│   │   └── Memristors_Presentation    # Slide deck summarizing the literature review
│
│   └── Instructions/                 
│       └── Instructions.pdf           # Original assignment guidelines
```

