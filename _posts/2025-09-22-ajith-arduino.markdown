---
layout: post
title:  "START A PROJECT WITH ATmega328p"
date:   2025-09-24
image:  nano/ajith.jpeg
tags:   Home Arduino
author: Ajith
---

# Blinking an External LED with ATmega328

## This project demonstrates how to blink an external LED using the ATmega328P microcontroller. It's a classic beginner-friendly example to get started with embedded programming and microcontroller interfacing.
🧰 Requirements
• 	ATmega328P microcontroller
• 	External LED
• 	A resistor
• 	Breadboard and USB Cable
• 	AVR toolchain (e.g., Atmel Studio, avr-gcc, or Arduino IDE)

![]({{ site.baseurl }}/images/nano/ajith.jpeg)

#CODE 
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




