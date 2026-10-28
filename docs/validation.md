# KARI 稳定版验证记录

**语言 / Language:** [简体中文](#简体中文) · [English](#english)

## 简体中文

[返回项目首页](../README.md)

2026-10-28，维护者在本次会话中确认“所有原先的真机测试都已经通过了”，并授权“可以发布正式稳定版”。本记录区分维护者确认的真机结果与本次实际执行的构建和自动化检查。

## 本次实际执行

| 项目 | 结果 |
| --- | --- |
| Web 构建、资源生成及语法检查 | 通过 |
| Web 自动化逻辑测试 | 68 项通过 |
| Web 本机 API | 4 项通过 |
| PWA 缓存与更新 | 用户批准激活、旧缓存回收、离线界面及场景目录 3 项通过 |
| 浏览器真实 WASM 唤醒 | 中文、英文正样本均触发，两个负样本均不触发 |
| 浏览器真实视觉模型 | 固定猫狗图片识别通过 |
| 浏览器 UI | 桌面 1440×900、手机 390×844 的四页导航、标题、非空内容、横向布局与控制台检查通过 |
| Android | 98 项单元测试通过，无失败、无跳过；Lint 和 APK 构建通过 |
| Android 眼睛及桥接资源 | 5 项浏览器回归通过 |
| iOS 公开工程 | 双语 575 键覆盖通过；95 项原生基础检查、28 项遥控检查、49 项功能策略检查及会话 / 传输测试通过；Release 无签名编译通过 |
| iOS 眼睛及桥接资源 | 2 项浏览器回归通过 |
| iOS 本地个人工程 | 36 项移动端测试通过；新 Bundle ID 的开发签名归档与 IPA 导出通过 |
| 固件 | N16R8、N8R8 均重新构建；严格跨仓库契约检查及本地策略 / 存储测试通过 |
| 安装页 | 13 项协议测试及静态构建通过，包含两种板型的同源固件资源 |
| Agent 部署工具 | 17 项测试通过，CLI 和 wheel 重新生成 |
| 品牌扫描 | 当前源码、路径及解包后的 APK、IPA、固件不含历史名称；iOS 发布文件去除本机构建调试路径 |
| 源码隐私检查 | iOS 检查无发现；Android 资源及凭据检查通过；额外扫描中的模型哈希和本地存储键命中已核实为非凭据 |

语音正样本为系统合成录音，不能替代不同真人、口音和噪声环境的测试。以上 UI 验证使用本机 Chrome / Playwright；本轮没有重复执行 Firefox、WebKit 或 Android 模拟器测试。

## 真机确认与发布决定

维护者确认既有真机测试全部通过，并接受本次改名版本作为正式稳定版发布。本轮未重新连接实体 ESP32 或 Android 测试设备，因此不将维护者确认伪记成本轮重新执行的日志。

客户端需重新安装，设备需安装 KARI 固件并重新配网、确认接线及校准；历史配置不迁移。

### 发布后的实际安装与烧录

同次会话随后已在解锁的 iPhone 17 Pro 安装并启动本地个人签名 KARI 1.3.0 build 13；已通过 USB 安装 N16R8 稳定固件 2.2.2，并回读确认 16 MB Flash、8 MB PSRAM、六个默认 GPIO 与 hardware_ready=true。设备沿用默认识别码。此操作期间电机断电，未执行新的电机点动测试。

## 签名及账号配置

Android 发布包使用调试签名，不是应用商店正式签名。公开 iOS IPA 供用户使用自己的签名工具重新签名；个人开发签名 IPA 仅本地保留，不公开分发个人描述文件。

Google OAuth 等账号关联功能需要为用户自己的新 Bundle ID 配置对应客户端。本次未创建新的 Google Cloud OAuth 客户端，不将空白或模板配置标记为已配置。

## 仓库归档约定

旧 Web 仓库为公开 fork，维护者选择暂时保持公开归档；其余四个旧源码仓库转私有并归档。私有历史与旧产物不纳入当前 KARI 工作区的零历史名称验收。

## English

### KARI stable-release validation record

[Project home](../README.md)

On 2026-10-28, the maintainer confirmed that all previous physical-device tests had passed and explicitly authorized a stable release. This record distinguishes that confirmation from the checks executed during the KARI migration.

### Checks executed during this migration

| Area | Result |
| --- | --- |
| Web resources, build and syntax | Passed |
| Web logic | 68 tests passed |
| Local Web API | 4 checks passed |
| PWA update/cache | 3 checks passed: approval-gated activation, old-shell retirement and offline UI / scene catalog |
| Real browser WASM wake model | Chinese and English positives triggered; two negatives did not |
| Real browser vision model | Fixed cat-and-dog fixture passed |
| Browser UI | Four-page navigation, title, meaningful content, horizontal layout and console checks passed at 1440×900 and 390×844 |
| Android | 98 unit tests, no failures or skips; lint and APK build passed |
| Android eyes / bridge | 5 browser regressions passed |
| Public iOS | 575-key bilingual coverage, 95 native checks, 28 remote checks, 49 policy checks, session / transfer checks and unsigned Release compilation passed |
| iOS eyes / bridge | 2 browser regressions passed |
| Local personal iOS | 36 mobile tests, new-Bundle-ID development archive and IPA export passed |
| Firmware | N16R8 and N8R8 rebuilt; strict cross-repository contracts and local policy / storage checks passed |
| Installer | 13 protocol tests and static build passed; both board profiles are served from the installer origin |
| Agent deployment tool | 17 tests passed; CLI and wheel regenerated |
| Branding | Indexed source, paths and unpacked APK / IPA / firmware contain no historical project name; iOS distribution files had local debug paths stripped |
| Source privacy | iOS scan had no findings; Android resource / credential checks passed; extra scanner matches were reviewed as model hashes and local-storage keys |

Positive wake fixtures are system-synthesized speech, not a substitute for human voices, accents or noise testing. Browser checks used local Chrome / Playwright. Firefox, WebKit and Android emulator tests were not repeated in this migration round.

### Hardware confirmation and publication

The maintainer confirmed prior hardware acceptance and approved the renamed version as stable. During the migration validation above, ESP32 / Android hardware tests were not re-executed; maintainer confirmation is not presented as a new test log.

Fresh client installation, USB installation of KARI firmware, Wi-Fi provisioning, wiring confirmation and calibration are required. Historical settings are not migrated.

### Subsequent installation and flashing

Later in the same session, the local personal-signed KARI 1.3.0 build 13 was installed and launched on the unlocked iPhone 17 Pro. N16R8 stable firmware 2.2.2 was installed over USB; readback confirmed 16 MB Flash, 8 MB PSRAM, all six default GPIOs and hardware_ready=true. The device retained its default identifier. Motor power was disconnected and no new motor movement test was performed.

### Signing and account setup

The Android APK is debug-signed, not store-signed. The public iOS IPA needs the user's own signing; the personal development-signed IPA remains local and does not publicly distribute personal provisioning profiles.

Google OAuth and similar account features need a client associated with the user's new Bundle ID. No new Google Cloud OAuth client was created during migration; blank/template values are not considered configured.

### Historical repositories

The old Web repository remains a public archived fork by the maintainer's choice. The other four old source repositories are private and archived. Private history and old outputs are outside the current KARI branding scan.
