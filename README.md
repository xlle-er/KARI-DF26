# KARI DF26

<p align="center">
  <img src="docs/assets/app-icon-rounded.png" alt="KARI 图标 / KARI app icon" width="128" height="128">
</p>

**语言 / Language:** [简体中文](#简体中文) · [English](#english)

## 简体中文

KARI 是由 ESP32-S3 底盘与 Web、Android 或 iOS 客户端组成的陪伴机器人项目。可先体验离线眼睛和人格，再连接机器人身体及自行配置的 AI 服务。

本仓库仅提供 README 和使用文档，通过链接连接各个独立模块，不包含软件源码、子模块或安装包。

## 开始使用

1. 阅读[首次安装与接线](docs/installation.md)，确认开发板、供电和电机接线。
2. 通过[部署工具](https://github.com/xlle-er/KARI-DF26-Skill)或[网页安装页](https://xlle-er.github.io/KARI-DF26-Firmware/)安装 KARI 固件。
3. 选择 [Web](docs/web.md)、[Android](docs/android.md) 或 [iOS](docs/ios.md) 客户端，重新配对并开始陪伴。
4. 遇到连接、权限或更新问题，查看[维护与排障](docs/troubleshooting.md)。

## 模块仓库与下载

正式稳定版本：Web / Android / iOS **1.3.0**，固件 **2.2.2**，部署工具 **0.2.0**。版本验证与维护者真机确认见[验证记录](docs/validation.md)。

| 模块 | 源码 | 下载 / 安装 |
| --- | --- | --- |
| Web | [KARI-DF26-WEB](https://github.com/xlle-er/KARI-DF26-WEB) | 按[Web 使用说明](docs/web.md)本机运行 |
| Android | [KARI-DF26-ANDROID](https://github.com/xlle-er/KARI-DF26-ANDROID) | [APK 发布入口](https://github.com/xlle-er/KARI-DF26-ANDROID/releases) |
| iOS | [KARI-DF26-IOS](https://github.com/xlle-er/KARI-DF26-IOS) | [Xcode 构建与签名](docs/ios.md) |
| 固件 | [KARI-DF26-Firmware](https://github.com/xlle-er/KARI-DF26-Firmware) | [固件发布入口](https://github.com/xlle-er/KARI-DF26-Firmware/releases) |
| Agent 部署工具 | [KARI-DF26-Skill](https://github.com/xlle-er/KARI-DF26-Skill) | [安装与使用](https://github.com/xlle-er/KARI-DF26-Skill#手动使用) |

模块统一使用 `main` 分支，独立构建与发布。下载前核对对应 Release 的验证状态及 SHA-256；发布入口不代表所有平台都已有可下载的正式版本。

## 硬件与行为边界

推荐 ESP32-S3 N16R8 开发板，也支持匹配固件的 N8R8；电机驱动采用 L298N，详细引脚见[接线说明](docs/installation.md)。使用数据 USB 线，ESP32 与驱动共地。

首次配置前断开电机电源，确认接线后架空车轮测试。视觉跟随为实验功能，不测量厘米距离，不提供避障或防跌落。未完成实体机器人验证的项目以各模块验证记录为准。

## 名称与新安装

界面品牌为 **KARI**，中文称呼“卡里”。默认语音唤醒为“你好卡里”或“Hey KARI”，需要在支持该功能的客户端显式开启。

本版本采用新的应用身份、配置存储和设备命名。需要重新安装客户端，通过 USB 安装配套 KARI 固件，重新配网并确认接线。不会读取历史应用或固件的配置。

[固件使用与更新](docs/firmware.md) · [开发入口](docs/development.md) · [本次验证状态](docs/validation.md)

## English

KARI is a companion robot project combining an ESP32-S3 chassis with a Web, Android or iOS client. Start with offline eyes and personality, then connect the robot body and an AI service you configure yourself.

This repository contains only the README, usage guides and necessary document artwork. It links to independent modules and contains no application source, submodules or installers.

### Getting started

1. Read [First installation and wiring](docs/installation.md) and confirm the board, power supply and motor wiring.
2. Install KARI firmware with the [deployment tool](https://github.com/xlle-er/KARI-DF26-Skill) or [web installer](https://xlle-er.github.io/KARI-DF26-Firmware/).
3. Choose the [Web](docs/web.md), [Android](docs/android.md) or [iOS](docs/ios.md) client, pair the robot again and start companionship.
4. See [Maintenance and troubleshooting](docs/troubleshooting.md) for connection, permission and update issues.

### Module repositories and downloads

Stable versions: Web / Android / iOS **1.3.0**, firmware **2.2.2**, deployment tool **0.2.0**. See the [validation record](docs/validation.md) for automated results and the maintainer's hardware confirmation.

| Module | Source | Download / installation |
| --- | --- | --- |
| Web | [KARI-DF26-WEB](https://github.com/xlle-er/KARI-DF26-WEB) | [Run locally](docs/web.md) |
| Android | [KARI-DF26-ANDROID](https://github.com/xlle-er/KARI-DF26-ANDROID) | [APK releases](https://github.com/xlle-er/KARI-DF26-ANDROID/releases) |
| iOS | [KARI-DF26-IOS](https://github.com/xlle-er/KARI-DF26-IOS) | [Build and sign in Xcode](docs/ios.md) |
| Firmware | [KARI-DF26-Firmware](https://github.com/xlle-er/KARI-DF26-Firmware) | [Firmware releases](https://github.com/xlle-er/KARI-DF26-Firmware/releases) |
| Agent deployment tool | [KARI-DF26-Skill](https://github.com/xlle-er/KARI-DF26-Skill) | [Manual setup](https://github.com/xlle-er/KARI-DF26-Skill#手动使用) |

All modules use `main` and build and release independently. Check each release's validation notes and SHA-256 before downloading; a releases link does not imply every platform has an immediately installable package.

### Hardware and behavior limits

An ESP32-S3 N16R8 board is recommended; N8R8 is supported with matching firmware. The chassis uses an L298N motor driver. See the [wiring guide](docs/installation.md) for GPIOs. Use a USB data cable and share ground between the ESP32 and driver.

Disconnect motor power for initial setup and lift the wheels before testing confirmed wiring. Visual following is experimental: it does not measure distance in centimeters, avoid obstacles or detect drop-offs. Consult the module validation records for the exact hardware coverage.

### Naming and fresh installation

The brand is **KARI**, pronounced “kah-ree”; the Chinese name is “卡里”. Default wake phrases are “你好卡里” and “Hey KARI”. Enable wake mode explicitly in a supported client.

This version has new application identities, storage keys and device names. Reinstall the client, install matching KARI firmware over USB, and configure Wi-Fi and wiring again. Historical application and firmware settings are not read.

[Firmware and updates](docs/firmware.md) · [Developer entry points](docs/development.md) · [Validation](docs/validation.md)
