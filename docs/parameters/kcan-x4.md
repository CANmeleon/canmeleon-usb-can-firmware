# CANmeleon KCAN X4 Firmware Features and Performance

KCAN X4 mode; requires a device with 4 CAN interfaces and a license for this mode.

## Communication capabilities

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN channels | 4 CAN / CAN FD channels supported | Each channel supports transmission and reception. |
| Frame formats | 11 / 29-bit IDs; Classic CAN 0–8 B, CAN FD up to 64 B | Classic RTR supported; CAN FD supports BRS enabled or disabled. |
| Classic CAN bit rate | Up to 1 Mbit/s | Configure the bus bit rate in the host software. |
| CAN FD data-phase bit rate | Up to 12 Mbit/s | Configure arbitration and data phases independently; use transceivers and bus wiring suitable for the selected rates. |

## Timestamps

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Hardware receive timestamps | Supported | Linux / SocketCAN can read hardware frame reception times. |
| Timestamp resolution (Linux / SocketCAN reception) | 1 µs | Read the hardware timestamp field to analyze intervals between received frames. |

## Software and APIs

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Host platforms | Windows / Linux supported | Use the corresponding KCAN driver and SDK. |
| Software and API | kcan-bus / KCANBasic supported | For frame transmission, reception and application development. |
