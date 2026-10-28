# iOS 使用

**语言 / Language:** [简体中文](#简体中文) · [English](#english)

## 简体中文

[返回项目首页](../README.md) · [iOS 源码与详细说明](https://github.com/xlle-er/KARI-DF26-IOS)

## 构建安装

准备 macOS、Xcode 和可用签名团队，部署目标为 iOS 15 或更新版本：

```sh
git clone https://github.com/xlle-er/KARI-DF26-IOS.git
cd KARI-DF26-IOS
cp Config/Signing.local.xcconfig.example Config/Signing.local.xcconfig
open KARI.xcodeproj
```

编辑本地配置，设置自己的 `DEVELOPMENT_TEAM` 和唯一的 KARI Bundle ID。选择 **KARI** scheme 和自己的 iPhone，等待 Swift Package 依赖解析后构建运行。签名配置、证书和设备信息不得提交仓库。

公开 iOS 工程不要求 Capacitor 或 Node.js 才能构建；仅修改生成资源时才需要 Node.js。个人自签名工程在本地单独维护，不在文档仓库分发。

## 使用

在机器人页主动扫描并连接 KARI 设备，配置人格和 AI 服务。按需允许蓝牙、局域网、相机、麦克风及语音识别权限。新 Bundle ID 需要重新授权和配置。

从中央播放按钮启动陪伴，横屏进入眼睛界面。需要前台语音唤醒时显式开启并选择语言；中文使用“你好卡里”，英文使用“Hey KARI”。实时音视频、蓝牙和本地识别须在真机验证。

Google 登录等功能与应用身份关联，必须为新的 Bundle ID 配置相应 OAuth 客户端及回调；没有配置时不要把登录功能标记为可用。普通 AI 服务凭据在应用设置中自行填写。

## English

### iOS usage

[Project home](../README.md) · [iOS source and detailed instructions](https://github.com/xlle-er/KARI-DF26-IOS)

### Build and install

Use macOS, Xcode and an available signing team. The deployment target is iOS 15 or newer:

```sh
git clone https://github.com/xlle-er/KARI-DF26-IOS.git
cd KARI-DF26-IOS
cp Config/Signing.local.xcconfig.example Config/Signing.local.xcconfig
open KARI.xcodeproj
```

Set your own `DEVELOPMENT_TEAM` and unique KARI Bundle ID in the local configuration. Select the **KARI** scheme and your iPhone, resolve Swift Package dependencies, then build and run. Do not commit signing configuration, certificates or device information.

The public project needs neither Capacitor nor Node.js for a normal Xcode build. Node.js is required only when regenerating bundled resources. The personal signing project is maintained locally and is not distributed in this documentation repository.

### Use

Scan and explicitly connect to KARI from the Robot page, then configure personality and an AI service. Grant Bluetooth, local-network, camera, microphone and speech-recognition permissions as needed. The new Bundle ID requires fresh permissions and settings.

Start companionship with the central play action and rotate to landscape for the eyes view. Enable foreground wake explicitly and choose a language: “你好卡里” or “Hey KARI”. Live media, Bluetooth and local speech recognition require physical-device testing.

Google login and similar account features are associated with application identity. Register an OAuth client and callback for your new Bundle ID. Without that configuration, do not mark login as available. Enter ordinary AI provider credentials in the app's settings.
