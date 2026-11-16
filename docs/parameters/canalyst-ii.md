# CANmeleon CANalyst-II Firmware Features and Performance

CANalyst-II mode; requires a device with 2 CAN interfaces and a license for this mode.

## Communication capabilities

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN channels | 2 Classic CAN channels supported | Each channel supports transmission and reception. |
| Frame formats | 11 / 29-bit IDs; Classic CAN 0–8 B | Supports data frames and remote frames (RTR). |
| Classic CAN bit rate | Up to 1 Mbit/s | Configure the bus bit rate in the host software. |

## Timestamps

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Hardware receive timestamps | Supported | Read frame timestamps through the ControlCAN receive API. |

## Typical communication performance

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| 8-byte frame rate (short-duration) | approximately 4,400 frames/s | Classic CAN at 1 Mbit/s; one bus, combined traffic in both directions. |
| 8-byte frame payload throughput (short-duration) | approximately 0.28 Mbit/s | Classic CAN at 1 Mbit/s; one bus, combined traffic in both directions. Counts only frame data fields. |

## Software and APIs

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Software | Chuangxin USB-CAN Tool supported | Select the device interface corresponding to CANalyst-II / USBCAN-2A / USBCAN-2C. |
| Development API | ControlCAN API supported | Use the Chuangxin ControlCAN library; select a ZLG firmware mode for ZLG software. |
| Linux development API | ControlCAN API supported | Use the Chuangxin Linux ControlCAN library. |

## Unsupported features and limitations

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN FD | Not supported | Select a CAN FD firmware mode when CAN FD is required. |
