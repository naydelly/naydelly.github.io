---
layout: project
type: project
image: img/bank3.png
title: "Bank Database Application in C"
date: 2024
published: true
labels:
  - C
  - Vim
summary: "I developed an application that manages a bank's records for ICS 212 - Program Structures using C."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
</div>

This project I programmed both the database and the user interface of the application. The user-interface displays a menu of options that a banker can choose from to manage the bank's records. The UI takes in input and displays records. The UI calls functions from the database. Some of the essential functions I wrote for the database include the addRecord, deleteRecord, findRecord, and printAllRecord functions. The database also has functions that read from and write to record files. 

This project heavily emphasizes the use of pointers and structures, which are the foundations of my database. This project demonstrates the use of Makefiles to execute the program.

My writefile function demonstrates 

```c
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```
