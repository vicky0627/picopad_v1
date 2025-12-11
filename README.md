# Picopad v1

Picopad v1 is a custom 4-key macropad powered by the Raspberry Pi Pico and configured using the POG software suite.  
The project uses KMK firmware for flexible layer handling, macros, and USB HID functionality.

---

## 🧰 Software Used

### **POG – KMK Keyboard Generator**
POG is a visual tool used to configure the pin layout, layers, keymaps, and to generate KMK firmware.

**POG Webpage:**  
https://pog.heaper.de

With POG, Picopad v1 can:
- Configure layers and shortcuts
- Toggle and momentary switch layers
- Generate KMK firmware automatically
- Flash the firmware to the Pico using WebSerial/WebUSB

---

## 🔌 Pin Mapping (Raspberry Pi Pico)

Picopad v1 uses the following GPIO pins for its 4 switches:

| Key | GPIO Pin |
|-----|-----------|
| Key 1 | GPIO 6 |
| Key 2 | GPIO 7 |
| Key 3 | GPIO 8 |
| Key 4 | GPIO 9 |

Additional connection:
- **GND** → common ground for all switches

Wiring is simple:
Each switch connects between **GPIO pin** and **GND**.


---

## 💡 Features

- 3-layer macropad
- One key to cycle through layers
- Customizable macros using POG + KMK
- USB Type-C port soldered manually to Pico test pads
- Compatible with Windows, macOS, and Linux

---

## 💡 Features

- 3-layer macropad
- One key to cycle through layers
- Customizable macros using POG + KMK
- USB Type-C port soldered manually to Pico test pads
- Compatible with Windows, macOS, and Linux

- ---

## 🛠️ Hardware

- Raspberry Pi Pico  
- 4 mechanical switches (Outemu)  
- Custom 3D-printed case  
- USB-C port wired to Pico TP1/TP2/TP3 + Pin 40  

---

## 📜 License
MIT (or your preferred license)
