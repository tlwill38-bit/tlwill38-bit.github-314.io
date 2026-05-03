---
title: Module's Block Diagram
tags:
- tag1
- tag2
---

## Overview

The Diagram below is for the sensing function on team 306 Subterranian Rover. 

Items mentioned are:
* power levels
* Type of sensor
* team connections
* Power source



## Block Diagram 

![Example of Indivial Block diagram ](FinalBlock(1).png)

## Decision Making

This block diagram presents the essential components required to build a functional Hall effect sensing system. All components are surface mounted to reduce the overall footprint and satisfy the design constraints of the board. Indicator LEDs are included to provide clear visual feedback during messaging, debugging, and general system verification.

The microcontroller selected for this design is the 48 pin PIC18F57Q43, chosen for its wide range of available GPIO pins, flexible peripheral set, and straightforward programming workflow. The device will be programmed using the MPLAB SNAP in‑circuit programmer, which supports quick iteration and reliable configuration during development.

Additional considerations such as power regulation, signal conditioning for the Hall sensor, and proper routing for communication lines were incorporated to ensure stable operation and smooth integration with the rest of the system.