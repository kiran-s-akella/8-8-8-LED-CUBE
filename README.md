# 8x8x8 LED Cube Using Arduino Uno

## Introduction
This project is an **8×8×8 LED Cube** controlled by an **Arduino Uno**. It creates stunning 3D animations using **512 LEDs**, providing an interactive way to learn about multiplexing, persistence of vision (POV), and embedded programming.

## Features
- Controlled by **Arduino Uno**
- Uses **multiplexing** to control 512 LEDs with fewer pins
- Displays **3D animations and patterns**
- Programs written in **Embedded C / Arduino IDE**
- Expandable and customizable

## Components Required
- **Arduino Uno**
- **512 LEDs (Common Cathode/Anode)**
- **8×8 matrix layers (hand-soldered or PCB-based)**
- **Transistor Arrays (e.g., ULN2803, BC547)**
- **Resistors (330Ω, 1kΩ, 10kΩ)**
- **Shift Registers (e.g., 74HC595)**
- **Driver ICs (e.g., TPIC6B595, 74HC138)**
- **Power supply (5V, 2A recommended)**
- **PCB or perfboard for wiring**

## Circuit Design
- The cube is arranged in **8 layers**, each containing **64 LEDs**.
- The **rows** are controlled via shift registers.
- The **columns** (layers) are switched using transistors.
- Multiplexing is used to light up one layer at a time at high speed, creating the illusion of a 3D display.

## Wiring and Connections
- **LED Cathodes** connected to **8 transistor switches** (one per layer)
- **LED Anodes** connected to **8×8 matrix controlled by shift registers**
- **Shift registers** connected to Arduino via **SPI or digital pins**
- **Transistor bases** controlled by Arduino digital pins

## Software Implementation
1. **Install Arduino IDE** and necessary libraries.
2. **Upload the code** to Arduino Uno.
3. **Control animations** using pre-defined patterns or customize animations in code.
4. **Run the cube**, adjusting delay and brightness settings.

## Code Example
```cpp
void setup() {
    pinMode(13, OUTPUT); // Example pin setup
}

void loop() {
    digitalWrite(13, HIGH);
    delay(500);
    digitalWrite(13, LOW);
    delay(500);
}
```

## How It Works
- The cube lights up LEDs **layer by layer** at a fast rate (POV effect).
- **Pre-programmed patterns** generate animations.
- The **Arduino sends signals** to shift registers and transistor drivers to turn on/off LEDs.

## Applications
- Interactive **3D LED animations**
- Learning **microcontroller programming**
- Electronics and **multiplexing experiments**
- Artistic **light displays**

## Future Enhancements
- Add a **Bluetooth/Wi-Fi module** for remote control
- Use **a more powerful microcontroller (ESP32, STM32)**
- Implement **audio-reactive LED patterns**

## Author
Designed by **[Your Name]** | Contact: **[Your Email]**

## License
This project is **open-source** and can be freely modified and shared.


