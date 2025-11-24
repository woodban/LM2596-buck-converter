# LM2596 Adjustable Buck Converter

This repository contains the schematic for an **adjustable DC-DC buck converter** based on the **LM2596HVT-ADJ** switching regulator.  
The circuit efficiently steps down a higher DC voltage to a lower, adjustable output voltage.

---

##  Overview

The LM2596 is a popular high-efficiency buck regulator capable of delivering up to **3A** output current.  
This design includes input/output filtering, a Schottky diode for fast switching, an adjustable feedback network, and an enable pin for power control.

---

##  Circuit Description

### **Main Components**

- **U1 – LM2596HVT-ADJ**  
  Adjustable switching regulator.  
  - Pin 1: VIN  
  - Pin 2: OUTPUT  
  - Pin 3: GND  
  - Pin 4: FB (Feedback)  
  - Pin 5: ON/OFF (Enable)

- **L1 – 33µH Inductor**  
  Smooths switching current and stores energy.

- **D1 – 1N5822 Schottky Diode**  
  Fast-recovery diode used for inductor flyback current.

- **C1 – 680µF Input Capacitor**  
  Reduces input ripple and stabilizes the supply.

- **C2 – 220µF Output Capacitor**  
  Filters output and reduces ripple.

- **R1 – 10kΩ & R2 – 5kΩ**  
  Feedback voltage divider used to set the output voltage.  
  Adjusting R1 changes Vout.

- **P1 (Input Connector)**  
  VIN+ / VIN−

- **P2 (Output Connector)**  
  VOUT+ / VOUT−

---

##  How the Circuit Works

1. DC input enters through **P1**.  
2. LM2596 switches internally at high frequency to step down voltage.  
3. **L1** and **D1** form the main power stage that converts the switching waveform into smooth DC.  
4. **R1 + R2** feed back a fraction of the output voltage to the FB pin to regulate the output.  
5. **C1 and C2** filter both input and output to minimize ripple.  
6. Regulated output is available through **P2**.

---

## 📷 Schematic

![LM2596 Buck Converter Schematic](<img width="645" height="361" alt="image" src="https://github.com/user-attachments/assets/e8b57a35-5327-4445-aff9-cb3dddfa58f5" />
)

---

##  Features

- Adjustable output voltage  
- High efficiency switching regulator  
- Large filtering capacitors  
- Suitable for up to **3A** loads (depending on cooling)

---

## 📦 Applications

- Battery-powered devices  
- Robotics and embedded systems  
- DIY power supplies  
- Microcontroller projects

---


