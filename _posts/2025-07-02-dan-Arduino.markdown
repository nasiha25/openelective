---
layout: post
title:  "Arduino"
date:   2025-07-05 
image:  nano/dan.jpeg
tags:   Home Microcontrollers
author: Dan
---
Arduino is an open-source electronics platform based on easy-to-use hardware and software. It consists of a family of microcontroller boards (such as Arduino Uno, Mega, Nano, etc.) and a software development environment (Arduino IDE) that allows users to write code in a simplified version of C/C++. The main goal of Arduino is to make electronics more accessible to artists, hobbyists, students, and anyone interested in creating interactive projects.

my arduino project-1

![]({{ site.baseurl }}/images/nano/dan.jpeg
*Minimalism*
```c
  
  #include <avr/io.h>

void setup() {
DDRD = 4;
DDRB = 32; 
while(true){
   PORTB = 0;
   PORTD = 4;  
   delay(100);
   PORTD = 0;
   PORTB = 32;
   delay(100);
   
}

}

void loop() {
  // put your main code here, to run repeatedly:

}
```



