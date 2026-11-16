# CANmeleon ZLG USBCAN-2E-U Firmware Features and Performance

ZLG USBCAN-2E-U mode; requires a device with 2 CAN interfaces and a license for this mode.

## Communication capabilities

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN channels | 2 Classic CAN channels supported | Each channel supports transmission and reception. |
| Frame formats | 11 / 29-bit IDs; Classic CAN 0–8 B | Supports data frames and remote frames (RTR). |
| Classic CAN bit rate | 5 kbit/s–1 Mbit/s | Configure the bus bit rate in the host software. |

## Timestamps

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Hardware receive timestamps | Supported | Read frame reception times through the ZLG API. |
| Timestamp resolution (ZLG API reception) | 100 µs | Frame reception timestamps use 100 µs steps. |

## Software and APIs

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Software | ZCANPRO / ZXDoc / CANtest supported | Install the ZLG driver and select the matching device model. |
| Development API | Windows / ZLG API supported | Use zlgcan.dll for application development. |

## Unsupported features and limitations

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN FD | Not supported | Select a CAN FD firmware mode when CAN FD is required. |
