# 固件使用与更新

**语言 / Language:** [简体中文](#简体中文) · [English](#english)

## 简体中文

[返回项目首页](../README.md) · [固件源码](https://github.com/xlle-er/KARI-DF26-Firmware) · [固件 Release](https://github.com/xlle-er/KARI-DF26-Firmware/releases) · [部署工具](https://github.com/xlle-er/KARI-DF26-Skill)

首次安装按[接线与安装](installation.md)通过 USB 完成。N16R8 和 N8R8 使用对应板型的清单与分段文件；不要混用。

## 设备管理

未配网时连接设备 `KARI-…` 热点访问 `http://192.168.4.1/`；配网后在同一局域网访问设备 IP。局域网服务为 `_kari._tcp`，设备 ID 为 `kari-<MAC>`，蓝牙名称为 `KARI Body`。

设备管理页提供配网、接线检查、方向校准与更新入口。接线未确认前电机禁用，配置或升级时先停车。

## 后续更新

使用对应 KARI Release 中的 OTA 应用文件与 SHA-256 清单，或设备面板的在线检查入口。USB 使用分段安装清单，OTA 使用应用包；不能互换。在线更新依赖新仓库已存在匹配 Release。

本次采用独立配置命名空间，不迁移历史配置。第一次安装后重新配网、确认 GPIO 并校准；之后 KARI 配套版本的配置保留行为以固件说明与测试记录为准。不要主动擦除整片 Flash 来处理普通连接问题。

## English

### Firmware usage and updates

[Project home](../README.md) · [Source](https://github.com/xlle-er/KARI-DF26-Firmware) · [Releases](https://github.com/xlle-er/KARI-DF26-Firmware/releases) · [Deployment tool](https://github.com/xlle-er/KARI-DF26-Skill)

Perform the first USB installation using [installation and wiring](installation.md). N16R8 and N8R8 require their matching manifests and segments; never mix board profiles.

### Device management

Before provisioning, join the device's `KARI-…` hotspot and open `http://192.168.4.1/`. After provisioning, use its current LAN IP from the same network. The mDNS service is `_kari._tcp`, the device ID is `kari-<MAC>`, and the advertised name follows the firmware's default suffix or custom name.

The management panel offers Wi-Fi, wiring checks, direction calibration and updates. Motors remain disabled until wiring is confirmed. Stop before changing configuration or upgrading.

### Later updates

Use the matching KARI release's OTA application and SHA-256 manifest, or the panel's online check. USB uses a segmented manifest; OTA uses an application image. They are not interchangeable. Online checks require a matching release in the new repository.

KARI uses separate configuration namespaces and does not migrate historical settings. After the first installation, provision Wi-Fi, confirm GPIOs and calibrate again. Later configuration-retention behavior follows the firmware's compatibility policy and test records. Do not erase the entire Flash to resolve ordinary connection problems.
