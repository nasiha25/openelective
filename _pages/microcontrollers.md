---
layout: page
title: Microcontrollers
permalink: /microcontrollers/
---

# Arduino Nano

***

## Pin maps

![]({{ site.baseurl }}/images/nano/nanomap.jpg)

## Exercise 1

![]({{ site.baseurl }}/images/nano/nanoled.jpeg)

```c
#include <avr/io.h>
void setup(){
  DDRB = 32; // set PB5 as an output pin 0b00100000
  while(true){
     PORTB= 32; //make PB5 HIGH (5Volts)
     delay(100);
     PORTB= 0; //make PB5 LOW (0 Volts)
     delay(100);
  }
}
void loop(){
  }
```