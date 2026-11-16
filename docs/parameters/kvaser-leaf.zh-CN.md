# CANmeleon Kvaser Leaf 固件特性与性能参数

Kvaser Leaf 模式；需配套具备 1 路 CAN 接口及对应模式授权的设备。

## 通信能力

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| CAN 通道 | 支持 1 路 Classic CAN | 每通道支持发送和接收。 |
| 报文格式 | 11 / 29 位 ID；Classic CAN 0–8 B | 支持数据帧和远程帧（RTR）。 |
| Classic CAN 速率 | 5 kbit/s–1 Mbit/s | 通过上位机设置总线速率。 |

## 时间戳

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| 接收硬件时间戳 | 不支持；接收采用软件时间戳 | 接收时间记录固件处理报文的时刻。 |
| 发送完成硬件时间戳 | 支持 | 通过 CANlib 开启 TXACK 后读取成功发送通知的时间戳。 |
| 时间戳分辨率（CANlib） | 默认 1 ms；可设置为 1 µs | 通过 canIOCTL_SET_TIMER_SCALE 设置时间戳步进。 |

## 软件配套

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| 配套软件 | 支持 CanKing | 安装 Kvaser 驱动。 |
| 开发接口 | 支持 Windows / Kvaser CANlib | 用于 Classic CAN 应用开发。 |

## 不支持的功能与使用限制

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| CAN FD | 不支持 | 需要 CAN FD 时选择相应 CAN FD 固件模式。 |
