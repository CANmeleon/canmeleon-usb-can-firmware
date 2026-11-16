# CANmeleon KCAN X4 固件特性与性能参数

KCAN X4 模式；需配套具备 4 路 CAN 接口及对应模式授权的设备。

## 通信能力

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| CAN 通道 | 支持 4 路 CAN / CAN FD | 每通道支持发送和接收。 |
| 报文格式 | 11 / 29 位 ID；Classic CAN 0–8 B，CAN FD 最高 64 B | 支持 Classic RTR；CAN FD 支持 BRS 开启 / 关闭。 |
| Classic CAN 速率 | 最高 1 Mbit/s | 通过上位机设置总线速率。 |
| CAN FD 数据速率 | 最高 12 Mbit/s | 仲裁段与数据段独立配置；需配套支持相应速率的收发器和总线布线。 |

## 时间戳

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| 接收硬件时间戳 | 支持 | Linux / SocketCAN 可读取报文硬件接收时间。 |
| 时间戳分辨率（Linux / SocketCAN 接收） | 1 µs | 读取硬件时间戳字段，用于分析报文接收时间间隔。 |

## 软件配套

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| 主机平台 | 支持 Windows / Linux | 使用配套 KCAN 驱动与 SDK。 |
| 配套软件与接口 | 支持 kcan-bus / KCANBasic | 用于报文收发和二次开发。 |
