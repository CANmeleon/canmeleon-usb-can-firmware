# CANmeleon Kvaser Leaf Firmware Features and Performance

Kvaser Leaf mode; requires a device with 1 CAN interfaces and a license for this mode.

## Communication capabilities

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN channels | 1 Classic CAN channels supported | Each channel supports transmission and reception. |
| Frame formats | 11 / 29-bit IDs; Classic CAN 0–8 B | Supports data frames and remote frames (RTR). |
| Classic CAN bit rate | 5 kbit/s–1 Mbit/s | Configure the bus bit rate in the host software. |

## Timestamps

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Hardware receive timestamps | Not supported; reception uses software timestamps | The receive timestamp records when the firmware processes the frame. |
| Hardware transmit-completion timestamps | Supported | Enable TXACK through CANlib to read timestamps from successful-transmission notifications. |
| Timestamp resolution (CANlib) | 1 ms by default; configurable to 1 µs | Configure the timestamp step with canIOCTL_SET_TIMER_SCALE. |

## Software and APIs

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Software | CanKing supported | Install the Kvaser driver. |
| Development API | Windows / Kvaser CANlib supported | For developing Classic CAN applications. |

## Unsupported features and limitations

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN FD | Not supported | Select a CAN FD firmware mode when CAN FD is required. |
