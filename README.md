# STM32 Demo PCB

A research‑grade demonstration board built around the **STM32F103C8T6** microcontroller, designed and simulated using **KiCad EDA 9.0.7**. This project explores the fundamentals of embedded hardware design — from regulated power delivery to USB communication and clock stability — with a focus on practical experimentation and signal integrity.

---

## 🔍 Overview
This PCB serves as a compact, educational platform for understanding STM32 architecture and peripheral interfacing. It combines:
- **AMS1117‑3.3V regulator** for stable power conversion from USB VBUS.
- **12 MHz crystal oscillator** ensuring precise clock synchronization.
- **USB Micro‑B interface** compliant with ST’s AN4879 application note.
- **Decoupling and filtering network** for low‑noise analog and digital operation.
- **Boot configuration and reset circuitry** for flexible firmware flashing.

---

## ⚙️ Design Objectives
- Demonstrate **best practices in mixed‑signal PCB layout** for microcontrollers.
- Validate **power integrity and EMI suppression** using ferrite bead filtering.
- Provide a **modular foundation** for firmware development and peripheral expansion.
- Encourage **open‑source collaboration** in embedded prototyping and education.

---

## 🧩 Detailed Design Steps
1. **Power Regulation**  
   AMS1117‑3.3 linear regulator converts USB 5 V to 3.3 V. Bulk capacitors (22 µF) and ceramic bypass capacitors ensure transient suppression and stable load response.  

2. **Clock Generation**  
   A 12 MHz crystal oscillator with matched load capacitors provides precise timing. Startup stability and jitter minimization were validated against STM32 datasheet recommendations.  

3. **Reset and Boot Configuration**  
   BOOT0 pin with pull‑down resistor allows flexible bootloader entry. NRST circuitry ensures reliable system reset during debugging and flashing.  

4. **USB Interface**  
   Differential D+/D– lines routed with impedance control. ESD protection and reference to ST’s **AN4879 USB hardware guidelines** ensure compliance and robustness.  

5. **Decoupling Network**  
   Each VDD pin is paired with 100 nF capacitors placed close to the package. Ferrite beads isolate analog and digital domains, reducing ground bounce and noise coupling.  

6. **Mounting & Expansion**  
   GPIO headers expose key pins for prototyping. Mechanical stability is ensured with four mounting holes, supporting modular expansion boards.  

---

## 🧪 Research Insights
This design was developed through exploration of:
- **Signal integrity modeling** for USB differential pairs.
- **Thermal and transient analysis** of linear regulators under varying load.
- **Ground plane optimization** for mixed analog‑digital domains.
- **Component selection trade‑offs** between cost, noise, and stability.


