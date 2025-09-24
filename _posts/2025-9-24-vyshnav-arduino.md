---
layout: post
title: "Arduino Nano"
date: 2025-09-24 
image: nano/nanomap.jpg
tags: Home Microcontrollers
author: Vyshnav

---

Arduino is an open-source electronics platform based on easy-to-use hardware and software. It's designed for anyone—students, hobbyists, or professionals—to build interactive projects. At the heart of Arduino is a microcontroller that can read inputs (like light on a sensor or a finger on a button) and turn them into outputs (like turning on an LED or starting a motor). With a simple programming environment and a wide range of compatible components, Arduino makes learning electronics and coding accessible and fun.



```c

#include<avr/io.h>

void setup() {
DDRD=4;
DDRB=32;
while(true)
  {
    PORTB=0;
    PORTD=4;
    delay(10000);
    PORTB=32;
    PORTD=0;
    delay(1000);
    
    

  }  
}

void loop() {
 

}

```


![]({{ site.baseurl }}/images/nano/vyshnav.jpeg)
