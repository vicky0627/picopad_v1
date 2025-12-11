# Picopad v1

Picopad v1 is a custom 4-key macropad built using the Raspberry Pi Pico.  
It uses **POG** to generate KMK firmware and manage layers, macros, and pin assignments.

The device supports multiple layers, a layer-cycle key, and Outemu mechanical switches mounted in a compact 3D-printed case with USB-C input.

---

## 🧰 Software Used — POG

POG is a visual firmware generator for KMK.  
It allows you to configure:

- Pins & switch layout  
- Layers and macros  
- Hold/tap functions  
- Layer switching  
- USB HID behaviors  

You don’t need to edit Python manually — POG generates the full KMK firmware automatically.

🔗 **POG Webpage:**  
https://pog.heaper.de

---

## 🔌 Pin Mapping (Raspberry Pi Pico)

Picopad v1 uses four GPIO pins for the switch matrix:

| Key | Pico GPIO Pin |
|-----|---------------|
| Key 1 | GPIO 6 |
| Key 2 | GPIO 7 |
| Key 3 | GPIO 8 |
| Key 4 | GPIO 9 |

All keys share a common **GND** connection.

### Wiring Diagram (Simple)

GPIO 6 ──┐
GPIO 7 ──┤── switches → GND
GPIO 8 ──┤
GPIO 9 ──┘

---

## 🔌 USB-C Wiring (Manual Soldering)

USB-C connector is wired to the Pico test pads:

| USB-C Pad | Pico Pad |
|-----------|----------|
| D+ | TP1 |
| D– | TP2 |
| Shield / Ground | TP3 |
| 5V | Pin 40 (VBUS) |

This allows direct USB-C input even when the Pico's original micro-USB port is not used.

---

## 🎛 Layers

Picopad v1 supports **3 layers**, controlled by one layer-cycle key.

The layer key cycles:

Layer 0 → Layer 1 → Layer 2 → back to Layer 0

This is implemented in POG using layer switching actions (`TO(1)`, `TO(2)`, `TO(0)`).

---

## 📂 Folder Structure

picopad_v1/
├── firmware/
│ ├── code.py
│ ├── keymap.py
│ ├── settings.toml
│ ├── pog.json
│ └── kmk/ (KMK firmware library)
├── images/ (device pictures)
└── README.md

---

## 📸 Images

### Top View
![Picopad Top](images/pic1.jpg)

### USB-C Side View
![Picopad USB Side](images/pic2.jpg)

---

## 🛠 Hardware Features

- **Raspberry Pi Pico** microcontroller  
- **4× Outemu mechanical switches** (plate-mounted)  
- **USB-C port** soldered directly to test pads (TP1, TP2, TP3, Pin 40)  
- **3D-printed custom case** for compact and clean layout  
- **KMK firmware** generated via POG  
- **Single key layer-cycle system** (Layer 0 → 1 → 2 → 0)

---
