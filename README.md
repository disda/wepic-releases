# WePic Releases

**WePic**（微图）Windows 安装包与应用内更新清单的公开发布仓库。

源码仓库为私有；本仓库只放可下载的构建产物与 `version.json`，供客户端检查更新。

## 下载

| 版本 | 说明 |
|------|------|
| [v0.1.8](https://github.com/disda/wepic-releases/releases/tag/v0.1.8) | 当前发布：x64 / x86 安装包 |

- **64 位**：`WePicSetup-<version>-x64.exe`
- **32 位**：`WePicSetup-<version>.exe`

也可打开右侧 **Releases** 选择历史版本。

## 更新清单

应用内更新读取本仓库根目录的 [`version.json`](./version.json)（另有国内镜像时可并行探测）。清单含版本号、发行说明、安装包 URL、大小与 SHA-256。

## 校验

下载后可用 PowerShell 核对 SHA-256，并与对应 Release 说明或 `version.json` 中的值比对：

```powershell
Get-FileHash .\WePicSetup-0.1.8-x64.exe -Algorithm SHA256
```

## 系统要求

- Windows 10 1903 或更高版本
- 安装包已随附 OpenSSL 1.1（AI HTTPS / 更新下载共用）与 VC++ 运行库等依赖
