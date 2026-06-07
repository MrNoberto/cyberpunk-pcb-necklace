# ⚡ Cyberpunk PCB Necklace | Wearable Tech by Noberto

https://github.com/user-attachments/assets/c0ebc530-f476-4e9b-a90a-751b6ec893ef


Welcome to the official repository of the **Cyberpunk PCB Necklace**, a high-fashion wearable hardware project designed and engineered by **Noberto** (Lucas). 

This project bridges the gap between Computer Engineering and modern aesthetic fashion, transforming a fully functional, diamond-shaped Printed Circuit Board (PCB) into a cyberpunk-chic daily accessory, complete with a gorgeous silver-plated chain.

---

## 🔬 Circuit Architecture & Engineering Challenge

The core design philosophy of this wearable was to achieve maximum visual impact (driving 12 high-brightness LEDs) while maintaining a highly compact, minimalist form factor. This presented a classic hardware bottleneck.

### 🛑 The Bottleneck
The brain of the operation is an **ATtiny MCU**. Due to its micro-sized footprint, the MCU simply does not possess enough I/O pins or the current sourcing capability to drive 12 bright LEDs directly without burning out or sacrificing luminosity.

### 🧩 The Workaround: MOSFET Switching
Instead of relying on the MCU to supply power directly to the LEDs, the architecture splits the 12 LEDs into **4 independent groups of 3**. 

* Each group draws its energy directly from the battery power rail through dedicated **MOSFETs**.
* The **ATtiny** acts purely as the maestro, pulsing specific pins to fire the MOSFET gates at precisely the right time, creating dynamic lighting patterns without overloading the controller.

### 🛡️ Circuit Protection & Stability
To ensure the MCU operates flawlessly and prevent any damage from floating states or reverse charge coming from the switching transistors:
* **Gate Resistors:** Integrated four **10k ohm resistors** between the MCU pins and the MOSFET gates.
* **Pull-Down Resistors:** Added four **10k ohm pull-down resistors** tied directly to GND, ensuring total signal stability and preventing accidental LED triggering.

### 🔋 Micro-Optimization: The Single-Resistor Trick
Instead of cluttering the diamond layout with individual current-limiting resistors for every single LED, the board layout was engineered to use just **one single 1.0-ohm (1206 package) resistor** for ALL 12 LEDs. This clever optimization kept the design ultra-compact, clean, and highly aesthetic without compromising safety or performance.

---

## 🛠️ Hardware Features
* **Form Factor:** Geometric Diamond-shaped PCB.
* **Architecture:** Surface-Mount Technology (SMT), 100% hand-soldered.
* **Brain:** ATtiny Microcontroller.
* **Power:** CR2032 Coin Cell Battery with an onboard toggle switch.
* **Chain:** Premium silver-plated chain for daily wear comfort.

---

## 📸 Media & Demos
<img width="746" height="797" alt="Captura de tela 2026-06-07 135626" src="https://github.com/user-attachments/assets/0ce742dd-2cbb-4398-bc59-9e5b4f941727" />
<img width="1227" height="831" alt="Captura de tela 2026-06-07 135528" src="https://github.com/user-attachments/assets/f3fa6cad-fcb4-4c5e-b52c-207c48cb565b" />
 
---
