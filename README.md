# CANmeleon USB-CAN/CAN FD Firmware — Catalog and Downloads

[English](README.md) · [简体中文](README.zh-CN.md)

CANmeleon USB-CAN/CAN FD firmware lets supported adapters connect to different CAN software ecosystems on Windows and Linux. This repository is the firmware selection and download hub: compare SocketCAN, PCAN, Kvaser, Vector VN16xx, ETAS ES582 and ZLG workflows, then install or switch firmware with CANmeleon Device Manager.

**[Download and install](#download-and-install)** · [Supported hardware](https://canmeleon.com/en/firmware/devices/) · [Device Manager](https://github.com/CANmeleon/canmeleon-device-manager) · [Full firmware guides](https://canmeleon.com/en/firmware/)

## Choose your firmware

For Linux SocketCAN, start with GS USB or KCAN and its matching driver. For existing Windows software, select the firmware matching its driver or API in the table below.

| CANmeleon firmware | Software or API workflow | Selection notes |
| --- | --- | --- |
| [KCAN X4](https://canmeleon.com/en/firmware/kcan/) | Windows WinUSB, kcan-bus and KCANBasic; Linux kcan driver / SocketCAN | Four-channel operation requires suitable hardware and licensing. |
| [GS USB](https://canmeleon.com/en/firmware/gs-usb/) | Windows WinUSB / EcuBus-Pro; Linux gs_usb / SocketCAN | Channel availability and software-controlled termination depend on hardware and package. |
| [PCAN-USB](https://canmeleon.com/en/firmware/pcan-usb/) | PCAN driver, PCAN-View and PCAN-Basic | Classic CAN. |
| [PCAN FD / Pro FD / X6](https://github.com/CANmeleon/canmeleon-pcanfd-firmware) | PCAN-View, PCAN-Basic, EcuBus-Pro and python-can | CAN/CAN FD availability and channels depend on mode, hardware, driver and licensing. |
| [Kvaser Leaf](https://canmeleon.com/en/firmware/kvaser-leaf/) | CanKing and CANlib in Leaf Light v2 mode | Classic CAN. |
| [Kvaser FD](https://canmeleon.com/en/firmware/kvaser-fd/) | Kvaser driver, CanKing and CANlib | CAN/CAN FD; 2xHS/4xHS modes depend on hardware, licensing and package. |
| [VN16xx](https://github.com/CANmeleon/canmeleon-VN16xx-firmware) | Windows Vector driver, CANoe, CANalyzer, CANape and vxlapi | VN1610/VN1640A modes and channel configurations depend on hardware, firmware version and licensing. |
| [ES582](https://github.com/CANmeleon/canmeleon-es582-firmware) | ETAS driver and INCA for CAN/CAN FD traffic and XCP/CCP calibration | Check the model, license and applicable package in Device Manager. |
| [ZLG USBCAN-II](https://canmeleon.com/en/firmware/zlg-usbcan-ii/) | ZCANPRO, CANtest and ControlCAN | Classic CAN; use the matching driver and library. |
| [ZLG USBCAN-2E-U](https://canmeleon.com/en/firmware/zlg-usbcan-2e-u/) | ZCANPRO, CANtest and ControlCAN | CAN 2.0; select USBCAN-2E-U in the software. |
| [ZLG USBCANFD](https://github.com/CANmeleon/canmeleon-zlg-usbcanfd-firmware) | ZLG driver and ZCAN API | CAN/CAN FD; device identity and channels depend on hardware and package. |
| [CANalyst-II](https://canmeleon.com/en/firmware/canalyst-ii/) | WinUSB, USB-CAN Tool and ControlCAN | Two Classic CAN channels; select USB-CAN2.0 / VCI_USBCAN2. |

The hardware supplies the connectors and physical channels; the active firmware determines the host driver and software interface. Devices with sufficient storage and applicable licensing can retain multiple firmware images and run one at a time.

## Features and performance by firmware

[Compare the 12 firmware parameter tables](docs/parameters/README.md): channel modes, bit rates, timestamps, typical throughput, software interfaces and limitations.

## Supported hardware

Commercial adaptation examples include Kunhong KHCM-series chips and derived hardware. The [device catalog](https://canmeleon.com/en/firmware/devices/) lists the firmware choices for each full model number, including KH-UCANFD-LITE-X2U, KH-UCANFD-PRO-X2U and KH-UCANFD-PRO-X4U. Other adapters, embedded modules and controller ICs have their own firmware selections.

Match the complete model number before downloading. Connect the device in Device Manager to confirm available firmware, modes, channel counts and storage. For pinouts and wiring, follow the catalog links to the corresponding model documentation.

## Download and install

| Resource | Link |
| --- | --- |
| Device Manager for Windows x64 | [Installer and portable ZIP](https://canmeleon.com/en/device-manager/#downloads) |
| Published G2 firmware package **8.15.2** | [Release notes on Gitee](https://gitee.com/sysmax/kpcfg4-canmeleon/releases/tag/8.15.2) · [KH-UCANFD-G2.zip](https://gitee.com/sysmax/kpcfg4-canmeleon/releases/download/8.15.2/KH-UCANFD-G2.zip) |
| GitHub release channel | [Releases](https://github.com/CANmeleon/canmeleon-usb-can-firmware/releases) |
| Installation and switching | [Firmware management guide](https://canmeleon.com/en/device-manager/firmware-management/) |
| Offline imports and recovery | [Updates and recovery](https://canmeleon.com/en/device-manager/updates-and-recovery/) |

The linked **8.15.2** G2 package requires Device Manager **0.8.1 or later**. Use the package applicable to your device; the download above is hosted on Gitee.

1. Connect a supported device and read its information in Device Manager.
2. Select a firmware release from **Firmware Catalog**, or use **Import firmware ZIP** with a complete downloaded release.
3. Select applicable firmware and review the required storage and pending changes.
4. Confirm installation and keep the device connected until writing completes.
5. Reconnect, verify the installed version and switch to the firmware you want to run.
6. Install its required host driver and configure the corresponding CAN software.

For a device in KH-Updater mode, use the recovery guide linked above.

## Open-source participation and commercial services

CANmeleon is a USB-CAN/CAN FD ecosystem for hardware makers, chip vendors and developers across automotive, industrial systems, robotics, marine and automation applications. Hardware from different manufacturers can join through a matching firmware port.

- **Open-source hardware:** participate in [CANmeleon-Hardware](https://gitee.com/sysmax/canmeleon-hardware). Its dual-channel and multi-channel reference designs are planned; use the [component manifest](https://gitee.com/sysmax/canmeleon-hardware/blob/master/OPEN_SOURCE_MANIFEST.yaml) for release availability.
- **Free firmware adaptation:** [submit an open-source board adaptation request](https://github.com/CANmeleon/canmeleon-usb-can-firmware/issues/new?template=open_hardware_adaptation.md) with the project URL, board revision, MCU and target firmware/API. The program applies to selected board/firmware combinations.
- **Hardware manufacturer solutions:** [contact CANmeleon](mailto:len2slaw@foxmail.com?subject=CANmeleon%20hardware%20integration) for USB-CAN/CAN FD software and firmware integration.
- **Chip platform porting and maintenance:** [discuss your chip platform](mailto:len2slaw@foxmail.com?subject=CANmeleon%20chip%20platform%20porting) and the CANmeleon firmware families and maintenance scope you need.
- **Custom firmware:** [send your requirements](mailto:len2slaw@foxmail.com?subject=CANmeleon%20custom%20firmware), including USB/CAN interfaces, host OS/API, features and schedule.

Free binary firmware and open-source firmware have separate access and licensing terms. [Explore the CANmeleon ecosystem and commercial adaptation examples](https://github.com/CANmeleon).

## Frequently asked questions

**Can I run several firmware types simultaneously?**

One firmware runs at a time. Storing several images depends on hardware, storage and licensing.

**Does a listed firmware work on every supported device?**

Each model has its own firmware and mode support. Use the hardware catalog and the connected device's applicability results.

**Does downloading firmware enable every mode?**

Available modes and channels depend on the device and its license as well as the package. Check them in Device Manager before installation.

**Does this repository contain firmware source code?**

This repository provides the catalog, documentation and binary-package download routes. Refer to the relevant component or release for licensing information.

## Support and related repositories

- [Firmware issues and requests](https://github.com/CANmeleon/canmeleon-usb-can-firmware/issues): include the model, firmware, driver, OS and CAN software versions, plus steps to reproduce.
- [Device Manager](https://github.com/CANmeleon/canmeleon-device-manager) for installation, connection and software-update issues.
- [VN16xx firmware](https://github.com/CANmeleon/canmeleon-VN16xx-firmware) for its hardware, modes and Vector software workflow.
- [Existing firmware discussions and issues on Gitee](https://gitee.com/sysmax/kpcfg4-canmeleon/issues).
