# CANmeleon PCAN Pro FD Firmware Features and Performance

PCAN Pro FD mode; requires a device with 2 CAN interfaces and a license for this mode.

## Communication capabilities

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN channels | 2 CAN / CAN FD channels supported | Each channel supports transmission and reception. |
| Frame formats | 11 / 29-bit IDs; Classic CAN 0–8 B, CAN FD up to 64 B | Classic RTR supported; CAN FD supports BRS enabled or disabled. |
| Classic CAN bit rate | Up to 1 Mbit/s | Configure the bus bit rate in the host software. |
| CAN FD data-phase bit rate | Up to 12 Mbit/s | Configure arbitration and data phases independently; use transceivers and bus wiring suitable for the selected rates. |

## Timestamps

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Hardware receive timestamps | Supported | Read frame timestamps through the PCAN-Basic receive API. |
| Hardware transmit-completion timestamps | Supported | Enable PCAN_ALLOW_ECHO_FRAMES to read timestamps from transmit echo frames. |
| Timestamp resolution (PCAN-Basic) | 1 µs | Received frames and transmit-completion echo frames both have timestamps in 1 µs steps. |

## Typical communication performance

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| 64-byte frame rate (short-duration) | approximately 7,600 frames/s | CAN FD with BRS; 1 Mbit/s arbitration / 8 Mbit/s data; one bus, combined request and response traffic in both directions. |
| 0-byte frame rate, one direction | approximately 20,800 frames/s | PCAN-Basic; standard-ID CAN FD frames with BRS; 1 Mbit/s arbitration / 8 Mbit/s data; one bus, one direction. |
| 8-byte frame rate, one direction | approximately 19,300 frames/s | PCAN-Basic; standard-ID CAN FD frames with BRS; 1 Mbit/s arbitration / 8 Mbit/s data; one bus, one direction. |
| 64-byte frame rate, one direction | approximately 10,100 frames/s | PCAN-Basic; standard-ID CAN FD frames with BRS; 1 Mbit/s arbitration / 8 Mbit/s data; one bus, one direction. |
| 64-byte frame payload throughput, one direction | approximately 5.17 Mbit/s | PCAN-Basic; standard-ID CAN FD frames with BRS; 1 Mbit/s arbitration / 8 Mbit/s data; one bus, one direction. Counts only frame data fields. |

## Software and APIs

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Software | PCAN-View supported | Install the PEAK PCAN driver. |
| Development API | Windows / PCAN-Basic supported | For developing CAN / CAN FD applications. |
