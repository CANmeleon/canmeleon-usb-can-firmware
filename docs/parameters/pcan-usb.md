# CANmeleon PCAN-USB Firmware Features and Performance

PCAN-USB mode; requires a device with 1 CAN interfaces and a license for this mode.

## Communication capabilities

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN channels | 1 Classic CAN channels supported | Each channel supports transmission and reception. |
| Frame formats | 11 / 29-bit IDs; Classic CAN 0–8 B | Supports data frames and remote frames (RTR). |
| Classic CAN bit rate | 5 kbit/s–1 Mbit/s | Configure the bus bit rate in the host software. |

## Timestamps

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Hardware receive timestamps | Supported | Read frame timestamps through the PCAN-Basic receive API. |
| Hardware transmit-completion timestamps | Supported | Enable PCAN_ALLOW_ECHO_FRAMES to read timestamps from transmit echo frames. |
| Timestamp resolution (PCAN-Basic) | approximately 42.7 µs | Received frames and transmit-completion echo frames use the same timestamp resolution. |

## Software and APIs

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Software | PCAN-View supported | Install the PEAK PCAN driver. |
| Development API | Windows / PCAN-Basic supported | For developing Classic CAN applications. |

## Unsupported features and limitations

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN FD | Not supported | Select a CAN FD firmware mode when CAN FD is required. |
