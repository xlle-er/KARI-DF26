# 固件使用与更新

[返回项目首页](../README.md) · [固件源码](https://github.com/xlle-er/KARI-DF26-Firmware) · [固件 Release](https://github.com/xlle-er/KARI-DF26-Firmware/releases) · [部署工具](https://github.com/xlle-er/KARI-DF26-Skill)

首次安装按[接线与安装](installation.md)通过 USB 完成。N16R8 和 N8R8 使用对应板型的清单与分段文件；不要混用。

## 设备管理

未配网时连接设备 `KARI-…` 热点访问 `http://192.168.4.1/`；配网后在同一局域网访问设备 IP。局域网服务为 `_kari._tcp`，设备 ID 为 `kari-<MAC>`，蓝牙名称为 `KARI Body`。

设备管理页提供配网、接线检查、方向校准与更新入口。接线未确认前电机禁用，配置或升级时先停车。

## 后续更新

使用对应 KARI Release 中的 OTA 应用文件与 SHA-256 清单，或设备面板的在线检查入口。USB 使用分段安装清单，OTA 使用应用包；不能互换。在线更新依赖新仓库已存在匹配 Release。

本次采用独立配置命名空间，不迁移历史配置。第一次安装后重新配网、确认 GPIO 并校准；之后 KARI 配套版本的配置保留行为以固件说明与测试记录为准。不要主动擦除整片 Flash 来处理普通连接问题。
