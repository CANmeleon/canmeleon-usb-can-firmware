# CANmeleon USB-CAN/CAN FD 固件 — 总览与下载

[English](README.md) · [简体中文](README.zh-CN.md)

CANmeleon 通过可切换的固件，让支持的 USB-CAN/CAN FD 硬件连接不同 CAN 软件生态。按使用场景选择固件，再通过设备管理器安装、更新或切换。本仓库承载固件总览和统一发布入口。

**[下载与安装](#下载与安装)** · [支持设备](https://canmeleon.com/zh/firmware/devices/) · [设备管理器](https://github.com/CANmeleon/canmeleon-device-manager) · [完整固件指南](https://canmeleon.com/zh/firmware/)

## 按软件需求选择固件

| CANmeleon 固件 | 软件或 API 路径 | 选用条件 |
| --- | --- | --- |
| [KCAN X4](https://canmeleon.com/zh/firmware/kcan/) | Windows WinUSB、kcan-bus、KCANBasic；Linux kcan 驱动 / SocketCAN | 四通道需要硬件和授权支持。 |
| [GS USB](https://canmeleon.com/zh/firmware/gs-usb/) | Windows WinUSB / EcuBus-Pro；Linux gs_usb / SocketCAN | 通道及软件终端电阻控制取决于硬件与固件包。 |
| [PCAN-USB](https://canmeleon.com/zh/firmware/pcan-usb/) | PCAN 驱动、PCAN-View、PCAN-Basic | 经典 CAN。 |
| [PCAN FD / Pro FD / X6](https://github.com/CANmeleon/canmeleon-pcanfd-firmware) | PCAN-View、PCAN-Basic、EcuBus-Pro、python-can | CAN/CAN FD 与通道取决于模式、硬件、驱动及授权。 |
| [Kvaser Leaf](https://canmeleon.com/zh/firmware/kvaser-leaf/) | Leaf Light v2 模式下的 CanKing、CANlib | 经典 CAN。 |
| [Kvaser FD](https://canmeleon.com/zh/firmware/kvaser-fd/) | Kvaser 驱动、CanKing、CANlib | CAN/CAN FD；2xHS/4xHS 模式取决于硬件、授权及固件包。 |
| [VN16xx](https://github.com/CANmeleon/canmeleon-VN16xx-firmware) | Windows Vector 驱动、CANoe、CANalyzer、CANape、vxlapi | VN1610/VN1640A 模式和通道配置取决于硬件、固件版本与授权。 |
| [ES582](https://github.com/CANmeleon/canmeleon-es582-firmware) | ETAS 驱动、INCA；CAN/CAN FD 收发及 XCP/CCP 标定 | 在管理器中核对型号、授权和适用固件包。 |
| [ZLG USBCAN-II](https://canmeleon.com/zh/firmware/zlg-usbcan-ii/) | ZCANPRO、CANtest、ControlCAN | 经典 CAN，使用匹配的驱动与库。 |
| [ZLG USBCAN-2E-U](https://canmeleon.com/zh/firmware/zlg-usbcan-2e-u/) | ZCANPRO、CANtest、ControlCAN | CAN 2.0，软件设备类型选择 USBCAN-2E-U。 |
| [ZLG USBCANFD](https://github.com/CANmeleon/canmeleon-zlg-usbcanfd-firmware) | ZLG 驱动、ZCAN API | CAN/CAN FD；识别名称和通道取决于硬件及固件包。 |
| [CANalyst-II](https://canmeleon.com/zh/firmware/canalyst-ii/) | WinUSB、USB-CAN Tool、ControlCAN | 双通道经典 CAN；选择 USB-CAN2.0 / VCI_USBCAN2。 |

硬件决定接口和物理通道，运行的固件决定电脑端驱动与软件接入方式。存储空间和授权允许时可保存多种固件，每次运行一种。

## 各固件特性与性能参数

[查看 12 种固件参数表](docs/parameters/README.zh-CN.md)：通道模式、速率、时间戳、典型吞吐、软件接口及功能限制。

## 支持硬件

[设备目录](https://canmeleon.com/zh/firmware/devices/)按完整型号列出可选固件，包括 KH-UCANFD-LITE-X2U、KH-UCANFD-PRO-X2U 和 KH-UCANFD-PRO-X4U。其他适配器、嵌入式模块与控制器芯片分别有其固件支持范围。

下载前核对完整型号，连接管理器后确认可用固件、模式、通道和存储。引脚、接线及硬件规格通过设备目录进入鲲弘文档查看。

## 下载与安装

| 资源 | 入口 |
| --- | --- |
| Windows x64 设备管理器 | [安装程序与便携 ZIP](https://canmeleon.com/zh/device-manager/#downloads) |
| 已发布 G2 固件包 **8.15.2** | [Gitee 版本说明](https://gitee.com/sysmax/kpcfg4-canmeleon/releases/tag/8.15.2) · [KH-UCANFD-G2.zip](https://gitee.com/sysmax/kpcfg4-canmeleon/releases/download/8.15.2/KH-UCANFD-G2.zip) |
| GitHub 发布入口 | [Releases](https://github.com/CANmeleon/canmeleon-usb-can-firmware/releases) |
| 安装与切换 | [固件管理指南](https://canmeleon.com/zh/device-manager/firmware-management/) |
| 离线导入与恢复 | [更新与恢复](https://canmeleon.com/zh/device-manager/updates-and-recovery/) |

以上 **8.15.2** G2 固件包要求设备管理器 **0.8.1 或更新版本**，下载托管于 Gitee。使用与设备匹配的固件包。

1. 连接支持设备，在管理器中读取信息。
2. 从固件目录选择版本，或导入已下载的完整固件 ZIP。
3. 选择适用固件，检查存储需求及待执行变更。
4. 确认安装，保持设备连接至写入完成。
5. 重新连接并核对版本，切换到需要运行的固件。
6. 安装对应电脑端驱动，配置目标 CAN 软件。

设备进入 KH-Updater 模式时，按上方恢复指南操作。

## 常见问题

**能同时运行多种固件吗？** 每次运行一种。能否保存多种固件取决于硬件、存储空间和授权。

**目录中的固件适用于所有设备吗？** 不同型号的固件与模式支持范围不同，请以设备目录及连接后的适用性结果选择。

**下载后会开放全部模式吗？** 可用模式与通道还取决于设备和授权，安装前在管理器中核对。

**仓库包含固件源码吗？** 本仓库提供目录、使用文档与二进制包下载入口，许可信息以对应组件或发布包为准。

## 支持与相关仓库

- [固件问题与需求](https://github.com/CANmeleon/canmeleon-usb-can-firmware/issues)：附型号、固件、驱动、系统及 CAN 软件版本和复现步骤。
- [设备管理器](https://github.com/CANmeleon/canmeleon-device-manager)：客户端安装、连接及软件更新问题。
- [VN16xx 固件](https://github.com/CANmeleon/canmeleon-VN16xx-firmware)：适用硬件、运行模式及 Vector 软件接入。
- [Gitee 已有固件问题记录](https://gitee.com/sysmax/kpcfg4-canmeleon/issues)。
