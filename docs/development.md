# 开发入口

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
