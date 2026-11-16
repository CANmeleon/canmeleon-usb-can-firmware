# CANmeleon Kvaser FD Firmware Features and Performance

2xHS / 4xHS modes supported; channel count depends on hardware and licensing. Performance and accuracy figures apply to the modes specified in the tables.

## Communication capabilities

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN channels | 2xHS: 2 channels; 4xHS: 4 CAN / CAN FD channels | Each channel supports transmission and reception; available modes depend on hardware and licensing. |
| Frame formats | 11 / 29-bit IDs; Classic CAN 0–8 B, CAN FD up to 64 B | Classic RTR supported; CAN FD supports BRS enabled or disabled. |
| Classic CAN bit rate | 5 kbit/s–1 Mbit/s | Configure the bus bit rate in the host software. |
| CAN FD data-phase bit rate | Up to 8 Mbit/s | Configure arbitration and data phases independently; use transceivers and bus wiring suitable for the selected rates. |
| Listen-only mode | Supported | Does not transmit frames or acknowledge frames on the bus in listen-only mode. |

## Timestamps

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Hardware receive timestamps | Supported | Read frame timestamps through the CANlib receive API. |
| Hardware transmit-completion timestamps | Supported | Enable TXACK through CANlib to read timestamps from successful-transmission notifications. |
| Timestamp resolution (CANlib) | 1 ms by default; configurable to 1 µs | Configure the timestamp step with canIOCTL_SET_TIMER_SCALE. |

## Typical communication performance

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| 64-byte frame rate (short-duration) | 2xHS: approximately 9,900 frames/s | CAN FD with BRS; 1 Mbit/s arbitration / 8 Mbit/s data; one bus, combined traffic in both directions. |
| 64-byte frame payload throughput (short-duration) | 2xHS: approximately 5.05 Mbit/s | CAN FD with BRS; 1 Mbit/s arbitration / 8 Mbit/s data; one bus, combined traffic in both directions. Counts only frame data fields. |

## Software and APIs

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Software | CanKing supported | Install the Kvaser driver. |
| Development API | Windows / Kvaser CANlib supported | For developing CAN / CAN FD applications. |
