# CANmeleon PCAN Pro FD 固件特性与性能参数

PCAN Pro FD 模式；需配套具备 2 路 CAN 接口及对应模式授权的设备。

## 通信能力

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| CAN 通道 | 支持 2 路 CAN / CAN FD | 每通道支持发送和接收。 |
| 报文格式 | 11 / 29 位 ID；Classic CAN 0–8 B，CAN FD 最高 64 B | 支持 Classic RTR；CAN FD 支持 BRS 开启 / 关闭。 |
| Classic CAN 速率 | 最高 1 Mbit/s | 通过上位机设置总线速率。 |
| CAN FD 数据速率 | 最高 12 Mbit/s | 仲裁段与数据段独立配置；需配套支持相应速率的收发器和总线布线。 |

## 时间戳

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| 接收硬件时间戳 | 支持 | 通过 PCAN-Basic 接收接口读取报文时间戳。 |
| 发送完成硬件时间戳 | 支持 | 开启 PCAN_ALLOW_ECHO_FRAMES 后，从发送回显读取时间戳。 |
| 时间戳分辨率（PCAN-Basic） | 1 µs | 接收报文和发送完成回显的时间戳均以 1 µs 为步进。 |

## 典型通信性能

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| 64 字节报文传输帧率（短时） | 约 7,600 帧/秒 | CAN FD，启用 BRS；1 Mbit/s 仲裁 / 8 Mbit/s 数据；单条总线、请求与应答双向合计。 |
| 0 字节报文单向传输帧率 | 约 20,800 帧/秒 | PCAN-Basic；CAN FD 标准帧，启用 BRS；1 Mbit/s 仲裁 / 8 Mbit/s 数据；单条总线、单向。 |
| 8 字节报文单向传输帧率 | 约 19,300 帧/秒 | PCAN-Basic；CAN FD 标准帧，启用 BRS；1 Mbit/s 仲裁 / 8 Mbit/s 数据；单条总线、单向。 |
| 64 字节报文单向传输帧率 | 约 10,100 帧/秒 | PCAN-Basic；CAN FD 标准帧，启用 BRS；1 Mbit/s 仲裁 / 8 Mbit/s 数据；单条总线、单向。 |
| 64 字节报文单向有效数据吞吐 | 约 5.17 Mbit/s | PCAN-Basic；CAN FD 标准帧，启用 BRS；1 Mbit/s 仲裁 / 8 Mbit/s 数据；单条总线、单向。仅计算报文数据字段。 |

## 软件配套

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| 配套软件 | 支持 PCAN-View | 安装 PEAK PCAN 驱动。 |
| 开发接口 | 支持 Windows / PCAN-Basic | 用于 CAN / CAN FD 应用开发。 |
