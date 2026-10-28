# Web 使用

**语言 / Language:** [简体中文](#简体中文) · [English](#english)

## 简体中文

[返回项目首页](../README.md) · [Web 源码与开发说明](https://github.com/xlle-er/KARI-DF26-WEB)

## 本机启动

准备 Node.js 22 或更新版本：

```sh
git clone https://github.com/xlle-er/KARI-DF26-WEB.git
cd KARI-DF26-WEB
npm ci
npm run build
cd backend
npm ci
npm start
```

在同一台电脑打开 `http://localhost:3000`。Web 项目直接位于仓库根目录，使用 `main` 分支。

不连接机器人或配置 AI 也能先体验离线陪伴。需要在线 AI 时，参考 `backend/.env.example` 创建本地 `.env`，填写自己的服务配置；不要提交或分享密钥。服务拆分见[部署文档](https://github.com/xlle-er/KARI-DF26-WEB/blob/main/docs/split-deployment.md)。

如果该地址曾安装历史 PWA，请先移除旧快捷方式并清除该站点缓存，再重新打开 KARI。新版本使用独立配置键，需要重新填写服务与设备设置。

## 连接与陪伴

从“机器人”页面扫描并主动选择 `KARI Body`；Web Bluetooth 需要兼容浏览器和 HTTPS / localhost。Wi-Fi 管理使用本机桥接和设备局域网地址，手机与设备须在可互通的网络中。

选择人格、界面语言和 AI 服务，按需授权麦克风、相机及蓝牙，再启动陪伴。语音唤醒在支持的浏览器中显式开启，使用“你好卡里”或“Hey KARI”。默认词表不包含历史称呼。

手机访问电脑服务需要配置 HTTPS 或合适的安全上下文，不能把手机的 `localhost` 当作电脑。模型及运行库按配置从后端加载，首次下载可能较慢；手动唤醒始终是排查入口。

身体运动需要明确允许；停止陪伴、断线或异常后重新检查状态。目标检测与跟随的限制见[功能说明](https://github.com/xlle-er/KARI-DF26-WEB/blob/main/docs/web-1.3.0/CAPABILITIES.md)。

## English

### Web usage

[Project home](../README.md) · [Web source and developer guide](https://github.com/xlle-er/KARI-DF26-WEB)

### Run locally

Install Node.js 22 or newer:

```sh
git clone https://github.com/xlle-er/KARI-DF26-WEB.git
cd KARI-DF26-WEB
npm ci
npm run build
cd backend
npm ci
npm start
```

Open `http://localhost:3000` on the same computer. The project is at the repository root on `main`.

Offline eyes and personality work without a robot or AI configuration. For online AI, create an untracked `backend/.env` using `backend/.env.example` and supply your own service settings. Never commit or share credentials. See [split deployment](https://github.com/xlle-er/KARI-DF26-WEB/blob/main/docs/split-deployment.md).

If this origin previously hosted an installed PWA, remove the old shortcut and clear that site's cache before opening KARI. New storage keys require entering service and device settings again.

### Connect and start companionship

Scan in the Robot page and explicitly choose the KARI device. Web Bluetooth requires a compatible browser and HTTPS / localhost. Wi-Fi management uses the localhost bridge and the device's LAN address; the client and robot must be on mutually reachable networks.

Choose personality, UI language and AI service, grant microphone / camera / Bluetooth permissions when needed, then start companionship. Enable wake mode explicitly in a supported browser and use “你好卡里” or “Hey KARI”; historical names are not included.

Accessing a computer's service from a phone requires HTTPS or another suitable secure context. The phone's `localhost` is not the computer. Models and runtimes load from the configured backend; initial downloads may take time. Use manual wake to troubleshoot microphone and recognition issues.

Explicitly allow body motion and recheck state after stop, disconnection or faults. See [capabilities](https://github.com/xlle-er/KARI-DF26-WEB/blob/main/docs/web-1.3.0/CAPABILITIES.md) for detection and following limits.
