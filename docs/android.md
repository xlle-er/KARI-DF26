# Android 使用

**语言 / Language:** [简体中文](#简体中文) · [English](#english)

## 简体中文

[返回项目首页](../README.md) · [Android 源码](https://github.com/xlle-er/KARI-DF26-ANDROID) · [APK 发布入口](https://github.com/xlle-er/KARI-DF26-ANDROID/releases)

## 安装

要求 Android 7.0 / API 24 或更新版本。从对应 Release 下载 KARI APK，核对 SHA-256，按系统提示允许当前来源安装。若 Release 尚无 APK，请按[模块构建说明](https://github.com/xlle-er/KARI-DF26-ANDROID#构建)构建。

应用 ID 为 `app.kari.companion`，作为新应用安装，需要重新配置服务、权限和机器人。调试签名包不等同于商店正式版。

## 使用

1. 打开 KARI，可先离线查看眼睛和人格。
2. 在设置中选择界面语言并按需配置自己的 AI 凭据；按需授权附近设备、麦克风和相机。部分旧系统扫描需要位置权限。
3. 在机器人列表扫描并选择 KARI 设备，确认设备已完成接线与配网。
4. 启动陪伴。需要语音唤醒时开启相应选项，中文说“你好卡里”，英文说“Hey KARI”。离线唤醒效果需以实际设备测试为准。
5. 遥控时按住移动、松手停止；先架空车轮核对方向。视觉跟随须明确选择目标并设置参考，不提供避障或防跌落。

真机 Live、BLE、模型与运动验收以[验证状态](validation.md)和模块记录为准。

## English

### Android usage

[Project home](../README.md) · [Source](https://github.com/xlle-er/KARI-DF26-ANDROID) · [APK releases](https://github.com/xlle-er/KARI-DF26-ANDROID/releases)

### Install

Requires Android 7.0 / API 24 or newer. Download the KARI APK from its release, check SHA-256 and permit installation from your chosen source. If an APK is unavailable, follow the [build instructions](https://github.com/xlle-er/KARI-DF26-ANDROID#构建).

The application ID is `app.kari.companion`. It installs as a new app: configure services, permissions and the robot again. A debug-signed package is not an app-store distribution.

### Use

1. Open KARI and try offline eyes and personality first.
2. Choose a UI language and configure your own AI credentials as needed. Grant nearby-device, microphone and camera permissions when requested; older Android versions may require location permission for scanning.
3. Scan in the robot list, select the KARI device and confirm its wiring and network setup.
4. Start companionship. Enable offline wake if desired: say “你好卡里” in Chinese or “Hey KARI” in English. Recognition quality must be assessed on your device.
5. Hold remote controls to move and release to stop. Lift the wheels before checking directions. Experimental following requires explicit target selection and a reference size; it provides no obstacle or drop-off detection.

See [validation](validation.md) and module records for physical Live, BLE, model and motion coverage.
