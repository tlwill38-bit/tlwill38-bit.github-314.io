---
title: API
tags:
- tag1
- tag2
---

All messages sent from this module follow the required framing format and use the correct team ID, sender ID, and receiver ID. The Hall effect subsystem uses the same message structure as the rest of the rover so that every module can interpret the data consistently.

The Hall effect module sends magnetic field readings as a numeric payload. The value is converted into a string before transmission so it remains compatible with the class rules for valid characters. Each message includes the team ID at the beginning and the required end markers so the receiving module can verify that the message is complete.

The Hall effect module supports two message types. The first is a periodic data message that sends the most recent magnetic field reading to the team. The second is a response message that is sent only when another module requests the current sensor value. Both message types use the same payload structure so the receiving module does not need separate parsing logic.

| Message Type | Full Message Format | Payload Description | Byte Count | Purpose |
|--------------|----------------------|---------------------|------------|---------|
| Sensor Data | AZTCvalueYB | value is the current magnetic field reading as a string | 2 bytes for AZ + 2 bytes for TC + N bytes for value + 2 bytes for YB | Sends the most recent Hall effect sensor reading |
| Data Request | AZTCREQYB | REQ indicates a request for the current sensor value | 2 bytes for AZ + 2 bytes for TC + 3 bytes for REQ + 2 bytes for YB | Requests the current Hall effect sensor reading |
| Response | AZTCvalueYB | value is the requested magnetic field reading | 2 bytes for AZ + 2 bytes for TC + N bytes for value + 2 bytes for YB | Returns the sensor value after receiving a request |

The API ensures that the Hall effect subsystem communicates correctly with the motor controller, the wireless module, and the human interface. It also ensures that the module meets the class requirements for message formatting, ID usage, and payload structure. This final version reflects the completed design and the way the sensor operates within the rover.