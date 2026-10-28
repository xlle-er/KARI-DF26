# 开发入口

**语言 / Language:** [简体中文](#简体中文) · [English](#english)

## 简体中文

[返回项目首页](../README.md)

各模块独立克隆，统一使用 `main`，没有子模块初始化步骤。文档仓库只负责使用说明。

| 模块 | 构建与测试说明 |
| --- | --- |
| Web | [README](https://github.com/xlle-er/KARI-DF26-WEB#readme) |
| Android | [README](https://github.com/xlle-er/KARI-DF26-ANDROID#构建) |
| iOS | [README](https://github.com/xlle-er/KARI-DF26-IOS#readme) |
| 固件 | [README](https://github.com/xlle-er/KARI-DF26-Firmware#固件开发维护者) |
| 部署工具 | [README](https://github.com/xlle-er/KARI-DF26-Skill#开发与验证) |

需要执行跨端协议检查时，将五个模块仓库按上述名称放在同一父目录。固件测试支持单仓库模式；整体验收必须使用严格跨仓库检查，避免缺少客户端时误判通过。

模块发布各自的二进制、校验和与验证报告，文档仓库只维护链接。私有配置保存在各模块忽略的本地文件中。

所有 README、教程和操作文档必须同时提供简体中文与 English。新增/修改步骤、命令、版本、链接或限制时同步更新两种语言；可共用代码示例，但不能仅翻译标题。第三方原始说明保留来源和许可证，并附维护者翻译。

## English

### Developer entry points

[Project home](../README.md)

Clone each module independently on `main`; no submodule initialization is needed. This documentation repository only provides usage guides.

| Module | Build and test documentation |
| --- | --- |
| Web | [README](https://github.com/xlle-er/KARI-DF26-WEB#readme) |
| Android | [README](https://github.com/xlle-er/KARI-DF26-ANDROID#构建) |
| iOS | [README](https://github.com/xlle-er/KARI-DF26-IOS#readme) |
| Firmware | [README](https://github.com/xlle-er/KARI-DF26-Firmware#固件开发维护者) |
| Deployment tool | [README](https://github.com/xlle-er/KARI-DF26-Skill#开发与验证) |

For cross-client protocol checks, put the five module repositories under one parent directory using their documented names. Firmware tests support standalone operation; integrated acceptance must use the strict cross-repository option so missing clients cannot be mistaken for passing checks.

Each module publishes its own binaries, checksums and validation notes. This repository maintains links only. Store private settings in each module's ignored local files.


All READMEs, tutorials and operating guides must provide Simplified Chinese and English. Update both versions whenever steps, commands, versions, links or limitations change. Code examples may be shared; translated headings alone are insufficient. Keep third-party originals, attribution and licenses, with a clearly attributed maintainer translation.
