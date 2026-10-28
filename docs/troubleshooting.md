# 维护与排障

**语言 / Language:** [简体中文](#简体中文) · [English](#english)

## 简体中文

[返回项目首页](../README.md)

| 问题 | 排查步骤 |
| --- | --- |
| 找不到机器人 | 确认已经安装 KARI 固件、供电正常；打开蓝牙及必要权限，主动重新扫描。历史应用配对记录不会迁移。 |
| Wi-Fi 管理失败 | 确认使用设备当前 IP；热点模式才使用 `192.168.4.1`。检查 2.4 GHz 网络、客户端隔离及局域网权限。 |
| 电机不动 | 先检查板型、接线确认、驱动供电和共地，再确认当前身体运动许可；不要绕过接线确认。 |
| 方向相反 | 架空车轮，在设备管理页短时校准左右交换和电机反向；先停止，再保存。 |
| 麦克风或相机不可用 | 检查系统权限；浏览器使用 HTTPS / localhost，其他应用可能占用设备。 |
| 唤醒无响应 | 确认功能开启、语言正确、应用前台运行，使用“你好卡里”或“Hey KARI”；先测试手动唤醒和麦克风。 |
| AI 无响应 | 检查服务地址、模型、网络和自己的凭据；诊断导出前确认已脱敏。离线陪伴不要求在线 AI。 |
| 在线更新失败 | 核对 KARI 仓库对应 Release、板型、清单与校验和；使用 USB 或本地更新前先阅读固件说明。 |
| USB 无法连接 | 使用数据线，关闭串口监视器，核对目标串口；按板型说明进入下载模式，不猜测多个设备中的目标。 |

模型、Live 会话和机器人运动仍须真机验证。各模块的源码、安装与问题入口见[项目首页](../README.md)。

## English

### Maintenance and troubleshooting

[Project home](../README.md)

| Problem | Checks |
| --- | --- |
| Robot not found | Confirm KARI firmware and power, enable Bluetooth and required permissions, then explicitly scan again. Historical app pairing records are not migrated. |
| Wi-Fi management fails | Use the current device IP; `192.168.4.1` applies to hotspot mode. Check 2.4 GHz support, client isolation and local-network permissions. |
| Motors do not move | Check board, confirmed wiring, driver power and common ground, then session motion permission. Do not bypass wiring confirmation. |
| Direction is reversed | Lift the wheels and use short tests to calibrate motor inversion / left-right swap. Stop before saving. |
| Microphone or camera unavailable | Check system permissions, HTTPS / localhost and whether another app owns the device. |
| Wake does not respond | Check enablement, language, foreground state and phrase (“你好卡里” / “Hey KARI”). Test manual wake and microphone first. |
| AI does not respond | Check provider URL, model, network and credentials. Redact diagnostic exports. Offline companionship needs no online AI. |
| Online update fails | Check the matching KARI release, board, manifest and checksum. Read the firmware guide before USB or local-file recovery. |
| USB cannot connect | Use a data cable, close serial monitors and identify the target port. Follow the board's bootloader instructions; never guess among multiple devices. |

Models, Live sessions and physical motion require hardware acceptance. Find source, installation and issue entry points on the [project home](../README.md).
