---
layout: post
title:  Microcontrollers
date:   2018-07-05 15:01:34 +0300
image:  nasi/Microcontroller.jpg
tags:   Home Microcontrollers
author: Nasiha
---


# Basics of Microcontrollers

## 1. Introduction
A **microcontroller** is a compact integrated circuit designed to perform specific control functions.  
It contains:
- **Processor (CPU)** – Executes instructions.
- **Memory** – Stores program code and data.
- **Input/Output (I/O) Ports** – Interfaces with external devices.

Microcontrollers are widely used in **embedded systems** such as home appliances, automobiles, medical devices, and industrial machines.

---

## 2. Key Features
- **Small Size & Low Power Consumption**
- **Integrated Peripherals** (Timers, ADC, UART, SPI, I²C, etc.)
- **Cost-Effective** for mass production
- **Real-Time Operation** capabilities

---

## 3. Common Microcontroller Families
- **8051 Series**
- **PIC Microcontrollers** (Microchip)
- **AVR** (Atmel/Microchip)
- **ARM Cortex-M Series**
- **MSP430** (Texas Instruments)

---

## 4. Basic Architecture
A typical microcontroller consists of:
1. **CPU** – Executes program instructions.
2. **Program Memory (ROM/Flash)** – Stores firmware.
3. **Data Memory (RAM)** – Temporary data storage.
4. **I/O Ports** – Digital and analog interfaces.
5. **Timers/Counters** – For time-based operations.
6. **Communication Interfaces** – UART, SPI, I²C, CAN, etc.

---

## 5. Applications
- **Consumer Electronics** – TVs, washing machines, microwaves
- **Automotive Systems** – Engine control, airbags, ABS
- **Industrial Automation** – Robotics, process control
- **Medical Devices** – Blood pressure monitors, ECG machines
- **IoT Devices** – Smart home systems, wearables

---

## 6. Advantages
- Low cost
- Compact size
- Energy efficient
- Easy to program for specific tasks

---

## 7. Getting Started with Microcontroller Programming
1. **Choose a Microcontroller** based on project needs.
2. **Set Up Development Tools**:
   - Compiler/IDE (e.g., MPLAB, Arduino IDE, Keil, STM32CubeIDE)
   - Programmer/Debugger
3. **Write the Program** in C, C++, or Assembly.
4. **Compile and Upload** to the microcontroller.
5. **Test and Debug** the application.

---

## 8. Summary
Microcontrollers are the backbone of modern embedded systems.  
Understanding their architecture, features, and programming is essential for designing efficient and reliable electronic products.
---

# Arduino Nano - Main Points

## Overview
- Small, breadboard-friendly microcontroller board.
- Developed by **Arduino.cc** in 2008.
- Based on **Microchip ATmega328P** MCU.
- Similar functionality to Arduino Uno but smaller.
- Powered via **USB Mini-B** or **9V battery**.


## Technical Specifications

### Nano R3 (Classic)
- MCU: ATmega328P (8-bit AVR, 16 MHz).
- Memory: 32 KB Flash, 2 KB SRAM, 1 KB EEPROM.
- I/O: 14 digital pins (6 PWM), 8 analog inputs.
- Operating voltage: 5V.
- Connectors: 30-pin headers, Mini-USB.


## Key Takeaway
The Arduino Nano evolved from the **ATmega328P-based Nano** into modern versions like the **Nano R4**, offering more processing power, memory, and connectivity options while keeping the compact Nano form factor.

![]({{ site.baseurl }}/images/nasi/Microcontroller.jpg)

**Now we have to start simple led-blink program using Arduino board in IDE software.**
- Requirements
• 	ATmega328P microcontroller
• 	External LED
• 	A resistor
• 	Breadboard and USB Cable
• 	AVR toolchain (e.g., Atmel Studio, avr-gcc, or Arduino IDE)

- connect LED’s positive end to the one end of resistor and other end to Nano’s digital pin D13 & negative end to Nano’s ground.To power Nano board, you can use USB cable or you can also connect an external power supply(5v-12v) by connecting positive pin to VIN and negative to the ground.Open the Arduino IDE and write the following program to blink an LED. After writing the program you may save it with a file name of your choice (find File–>Save on menu bar of IDE)

Select the Arduino board type in your IDE. here we are using an Arduino Nano board. To choose the board, find Tools on menu bar. Choose the option “Board” – and select your correct Arduino board.

###CODE 
```C

void setup() {
  DDRD = 4;
  DDRB = 32;
  while(true){
    PORTD = 4;
    delay(500);
    PORTD = 0;
    PORTB = 32;
    delay(500);
    PORTB = 0;
    
    
  }
}

void loop() {
}

```

![]({{ site.baseurl }}/images/nano/nasiha.jpeg)












