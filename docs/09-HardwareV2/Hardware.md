---
title: HardWare 2.0
---

## Improved Hall Effect Sensor Integration

In the first version, the Hall effect sensor required breakout boards because of routing limitations and time pressure. This added extra wiring and introduced noise that affected readings. In Version 2.0, the sensor would be fully integrated onto the PCB using a surface mount package. The design would include proper filtering, a clean analog ground path, and careful routing to keep the sensor clear. This would create more stable measurements and reduce the chance of mechanical failure.

## Improved Microcontroller Pin Planning

The first version required several late changes because some pins had restrictions that were not obvious at the start. Version 2.0 would begin with a clear pin planning process that accounts for analog inputs, UART communication, LED indicators, and debugging needs. This would prevent conflicts and reduce the need for last minute rewiring or code changes.

## Dedicated Test Points and Jumpers

Debugging the first version was difficult because there were not enough test points. Version 2.0 would include labeled pads for power, communication lines, and sensor outputs. Jumper points would allow subsystems to be isolated during troubleshooting. This would make it easier to track down issues without removing components or cutting traces.

## Summary

Hardware Version 2.0 focuses on creating a more stable and maintainable design. By improving sensor integration, power distribution, microcontroller planning, and mechanical protection, the rover becomes more reliable and easier to work with. These changes directly support the rover’s mission by ensuring consistent Hall effect sensing, dependable communication, and smoother operation in underground environments.