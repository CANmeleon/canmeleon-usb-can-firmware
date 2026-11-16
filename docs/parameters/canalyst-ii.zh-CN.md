# CANmeleon CANalyst-II 固件特性与性能参数

CANalyst-II 模式；需配套具备 2 路 CAN 接口及对应模式授权的设备。

## 通信能力

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| CAN 通道 | 支持 2 路 Classic CAN | 每通道支持发送和接收。 |
| 报文格式 | 11 / 29 位 ID；Classic CAN 0–8 B | 支持数据帧和远程帧（RTR）。 |
| Classic CAN 速率 | 最高 1 Mbit/s | 通过上位机设置总线速率。 |

## 时间戳

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| 接收硬件时间戳 | 支持 | 通过 ControlCAN 接收接口读取报文时间戳。 |

## 典型通信性能

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| 8 字节报文传输帧率（短时） | 约 4,400 帧/秒 | Classic CAN，1 Mbit/s；单条总线、双向合计。 |
| 8 字节报文有效数据吞吐（短时） | 约 0.28 Mbit/s | Classic CAN，1 Mbit/s；单条总线、双向合计。仅计算报文数据字段。 |

## 软件配套

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| 配套软件 | 支持创芯 USB-CAN Tool | 选择 CANalyst-II / USBCAN-2A / USBCAN-2C 对应设备接口。 |
| 开发接口 | 支持 ControlCAN API | 使用创芯 ControlCAN 库；ZLG 软件请选择 ZLG 固件模式。 |
| Linux 开发接口 | 支持 ControlCAN API | 使用创芯 Linux ControlCAN 库。 |

## 不支持的功能与使用限制

| 参数 | 能力 / 数值 | 备注 |
| --- | --- | --- |
| CAN FD | 不支持 | 需要 CAN FD 时选择相应 CAN FD 固件模式。 |
