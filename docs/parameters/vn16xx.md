# CANmeleon VN16xx Firmware Features and Performance

VN1610 / VN1640 modes supported; select the channel count according to hardware and licensing.

## Communication capabilities

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN channels | VN1610: 2 channels; VN1640: 4 CAN / CAN FD channels | Each channel supports transmission and reception; this table covers CAN-channel modes. |
| Frame formats | 11 / 29-bit IDs; Classic CAN 0–8 B, CAN FD up to 64 B | Classic RTR supported; CAN FD supports BRS enabled or disabled. |
| Classic CAN bit rate | 5 kbit/s–1 Mbit/s | Configure the bus bit rate in the host software. |
| CAN FD data-phase bit rate | Up to 10 Mbit/s | Configure arbitration and data phases independently; use transceivers and bus wiring suitable for the selected rates. |
| Custom bit timing | Configurable bit rate, sample point and SJW | Configure these in the host software; the firmware adapts automatically. |
| Errors and node status | Error events, transmit / receive error counters and Bus-Off status reporting supported | Diagnose conditions such as missing ACKs and mismatched bit rates. |
| Bus-Off recovery | Recovery through a host-initiated reset supported | Communication resumes after resetting or reactivating the channel. |
| ISO-TP / UDS integration | Single-session diagnostic communication supported | Use with host diagnostic software. |
| Termination control | Software-controlled termination supported | Configure in Device Manager; requires hardware with software-controlled termination. |
| Bus load | Bus-load display supported | The typical difference from the value displayed with Vector hardware is no more than 1 percentage point. |
| Listen-only mode | Supported | Does not transmit frames or acknowledge frames on the bus in listen-only mode. |

## Timestamps

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Hardware receive timestamps | Supported | Records frame reception times for analyzing intervals between frames. |
| Hardware transmit-completion timestamps | Supported | Records actual frame transmission completion times. |
| Timestamp accuracy within one device | 1 µs | For comparing frame times across CAN channels within the same device. |
| Multi-device software synchronization accuracy | &lt; 10 µs | Vector specifies a typical software synchronization accuracy of 50 µs for its VN1610. |
| Reading timestamps in CAPL | time_ns supported (nanosecond units) | Read frame timestamps and calculate time intervals. |
| Timestamp resolution (XL API) | approximately 8 µs | Read frame timestamps through the corresponding Vector driver. |

## Typical communication performance

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| 8-byte frame rate, one direction | approximately 23,000 frames/s (short-duration) | Standard-ID CAN FD frames with BRS; 1 Mbit/s arbitration / 8 Mbit/s data; one bus, one direction. |
| 64-byte frame receive rate | approximately 10,100 frames/s | Standard-ID CAN FD frames with BRS; 1 Mbit/s arbitration / 8 Mbit/s data; one bus, one direction. |
| 64-byte frame payload throughput | approximately 5.18 Mbit/s | Same bit-rate configuration as the preceding row; one bus, one direction; counts only the data fields of received frames. |

## Software and APIs

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| Host platform and development API | Windows / Vector XL API supported | Uses the Vector driver for host-software integration and application development. |
| CANoe / CAPL | CAN transmission, reception, transmit-completion echo and status queries supported | — |
| Application software | CANoe / CANalyzer / CANape supported | Install the Vector driver. |

## Differences from Vector hardware and unsupported features

| Parameter | Capability / value | Notes |
| --- | --- | --- |
| CAN FD data-phase bit rate | Up to 10 Mbit/s | Vector specifies up to 8 Mbit/s for its VN1610. Higher-speed communication requires suitable transceivers and bus wiring. |
| TX Self-ACK | Not supported | Transmission requires another node to acknowledge frames; without ACKs, transmission is retried and subsequent frames may wait. |
| Restricted output mode | Not supported | Selecting Restricted still operates in normal mode. |
| Transceiver operating modes | Normal mode only | Selecting another transceiver mode leaves the device in normal transmit/receive operation. |
| Active error-frame transmission / fault injection | Not supported | Vector's VN1610 supports active error-frame transmission; this firmware supports error detection, error counters and Bus-Off status reporting. |
| Classic CAN triple sampling | Not supported; uses single sampling | Select single sampling in your project. |
