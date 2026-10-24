# WePic Releases

WePic Windows 与 macOS 的公开安装包和共同更新清单。源码在独立私有仓库维护。

## 下载

打开 [最新发布](https://github.com/disda/wepic-releases/releases/latest) 下载安装包：

- Windows x64：`WePicSetup-<version>-x64.exe`；x86：`WePicSetup-<version>.exe`。要求 Windows 10 1903 或更新版本。
- Mac Apple Silicon：`WePic-<version>-<build>-macOS-arm64.dmg`。当前 build 120 要求 macOS 13.4 或更新版本；拖入应用程序后启动。
- ZIP 用于 Mac 应用内更新，首次安装请选择 DMG。旧 Mac 专用清单版本请先手动安装一次共用清单版本。

## 更新清单与日志

Windows 和 Mac 共用根目录 [version.json](./version.json)。`notes` 与 `changelog` 是共同更新记录，Release 正文由相同数据生成，不另维护 Mac JSON。

Mac 使用 [version.json.sig](./version.json.sig) 验证整个清单的发布者签名，然后检查 ZIP 大小、SHA-256 与应用完整性。Windows 兼容字段保留原安装器信息。默认发布者签名与 Apple 公证是不同机制；当前 Mac 包为 ad-hoc 代码签名，尚未 Apple 公证。

更新请在“设置 → 关于”中检查。v0.1.11 为首个公开版本，仅保留当前安装包；下载摘要可与 version.json 或 DMG 的 `.sha256` 文件核对。
