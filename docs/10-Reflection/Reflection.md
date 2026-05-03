---
title: Reflection
---
## Review of Modules Success

I successfully integrated the Hall effect sensor into the subterranean rover and developed the firmware needed to read, process, and transmit magnetic field data through our team’s communication system. I also implemented LED feedback for debugging, configured the PIC microcontroller peripherals, and validated the sensor’s behavior under different magnetic conditions. However, I did not fully achieve my goal of keeping the entire subsystem surface‑mount. Time constraints and routing limitations led me to rely on breakout boards for certain components, which added bulk and made debugging more complicated. 

## Module Start Up and Microcontroller
One of the biggest lessons was learning the PIC microcontroller quickly and understanding how its pin mapping, analog settings, and peripheral configurations affect the entire design. Planning pin assignments early is essential, especially when certain pins have hidden restrictions. I also learned the value of writing small test programs outside the main project to build confidence with the toolchain and catch mistakes before they become major setbacks. Sometimes the issue is as simple as a missing capacitor, and sometimes it is as simple a dissconected wire.

1. Learn the microcontroller early by writing small test programs before integrating anything into the main rover code.

2. Study the pinout carefully and check for hidden restrictions such as analog‑only pins, remappable peripherals, or pins that default to special functions.

3. Confirm every pin configuration in both the datasheet and the device family reference manual because one source alone is not always enough.

4. Build a simple LED blink test first to confirm that the chip is powered, clocked, and programmable before adding sensors or communication.

5. Test the Hall effect sensor separately on a breadboard or breakout before committing it to the PCB.

6. Double‑check analog settings, TRIS registers, and digital/analog mode selections because a single incorrect bit can make a sensor appear “dead.”

7. Keep your UART communication simple at first and verify it with a known‑good device before integrating it into the team protocol.

8. Add test pads or jumper points so you can isolate the sensor, disconnect subsystems, and debug without desoldering half the board.

9. Expect to reflash the microcontroller many times and keep your programming header accessible.

10. When something does not work, check power, ground, and continuity first because most early failures come from wiring or soldering, not code.

11. Practice reading the sensor output in a controlled environment before testing it inside the rover.

12. Save working versions of your code so you can revert when a new change breaks something unexpectedly.

13. Do not assume the issue is software; sometimes it is a missing capacitor, a noisy line, or too much solder paste causing a short.

14. Build confidence with the toolchain by experimenting outside the main project so you are not learning under pressure.

## Lessons Learned
Coding early is critical, and no detail in a communication protocol is too small to ignore, communicate with the team. Testing UART messaging early and often prevents last‑minute chaos. Adding jumper points and test pads makes debugging far easier and protects the circuit during development. Anything that can break will break, so isolating subsystems is essential. Datasheets are helpful, but they are not infallible, and footprints are not always trustworthy. Documenting successes matters because progress disappears quickly when you are deep in troubleshooting.

## Recomendations

* Plan ahead and start early because this course rewards preparation, not last‑minute work.

* Test communication protocols with your team early to avoid integration issues later.

* Add jumper points and test pads to make debugging easier and protect your circuit during development.

* Expect things to break and design your subsystem so failures do not cascade into other modules.

* Document your progress because successes are easy to forget when troubleshooting dominates your time.