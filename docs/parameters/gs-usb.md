# CANmeleon GS USB Firmware Features and Performance

GS USB mode; channel count depends on the device model and licensing.

## Communication capabilities

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN channels | 1 / 2 / 4 CAN / CAN FD channels supported | The number of available channels depends on the device model and licensing. |
| Frame formats | 11 / 29-bit IDs; Classic CAN 0–8 B, CAN FD up to 64 B | Classic RTR supported; CAN FD supports BRS enabled or disabled. |
| Classic CAN bit rate | Up to 1 Mbit/s | Configure the bus bit rate in the host software. |
| CAN FD data-phase bit rate | Up to 8 Mbit/s | Configure arbitration and data phases independently; use transceivers and bus wiring suitable for the selected rates. |
| Listen-only and loopback modes | Listen-only mode and internal loopback supported | Listen-only mode does not acknowledge bus frames; internal loopback is for local transmit/receive debugging. |
| Termination control | Software enable / disable of termination supported | Requires software-controlled termination hardware; the setting applies to the current session. |
| Classic CAN raw DLC 9–15 | Supported | Data frames still carry 8 data bytes; the original DLC value is preserved. |

## Timestamps

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Hardware receive timestamps | Supported | Enable hardware timestamp mode to read frame reception times. |
| Hardware transmit-completion timestamps | Supported | Read actual transmission completion times from transmit-completion echo frames. |
| Timestamp resolution (WinUSB / SocketCAN) | 1 µs | Use hardware timestamps; on SocketCAN, read the hardware timestamp field. |

## Typical communication performance

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| 8-byte frame rate, one direction (short-duration) | approximately 22,000 frames/s | Windows WinUSB; one bus and one direction on a four-channel device; standard-ID CAN FD frames with BRS; 1 Mbit/s arbitration / 8 Mbit/s data. |

## Software and APIs

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Linux | SocketCAN supported | Use the gs_usb driver. |
| Windows | EcuBus supported | Use the GS USB device interface. |

## Unsupported features and limitations

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| One-shot transmission / triple sampling / non-ISO CAN FD | Not supported | Use automatic retransmission, single sampling and ISO CAN FD. |
