# NeoClash 下载

基于 sing-box 的原生代理客户端。本仓库提供 Windows 和 macOS 安装包、版本说明与 SHA256 校验文件。

## Windows · x64 / ARM64 1.3.53

| 电脑 | 安装包 | 完整目录 ZIP |
| --- | --- | --- |
| Windows 10/11 · Intel / AMD 64 位 · 1.3.53（.NET Framework 4.8+） | [下载 x64 Setup.exe](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.53/NeoClash-1.3.53-Windows-Native-x64-Setup.exe) | [x64 ZIP](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.53/NeoClash-1.3.53-Windows-Native-x64.zip) |
| Windows 11 ARM64 · 1.3.53（.NET Framework 4.8.1+） | [下载 ARM64 Setup.exe](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.53/NeoClash-1.3.53-Windows-Native-arm64-Setup.exe) | [ARM64 ZIP](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.53/NeoClash-1.3.53-Windows-Native-arm64.zip) |

正常退出托盘中的旧版，运行对应架构 Setup，覆盖安装到原目录后打开 NeoClash。订阅和设置会保留。也可以通过应用内「更新」下载安装。从 1.3.46 发起更新时，按提示手动打开新版。从 1.3.47 或更高版本发起的更新会在自检通过后自动重开。Electron 用户使用 Setup 迁移。

1.3.53 支持五种界面语言，代理首页新增「检查并恢复」，默认每日代理流量超过 5 GB 时发送系统通知，阈值可在设置中调整。

本次更新覆盖 Windows x64 与 ARM64。

保留可选 TUN 与企业 VPN 会话隔离。Windows EXE / Setup 未做 Authenticode 签名。TUN 和企业引擎的既有管理员授权要求不变；真实企业登录与业务访问仍需在目标电脑确认。

## macOS 1.2.62 · Apple Silicon

macOS 1.2.77 在启动时可能闪退，已暂停推送。修复版验证期间可使用原有可运行版本。

[下载 NeoClash-1.2.62.dmg](https://github.com/niujt/NeoClash-Releases/releases/download/neoclash-v1.2.62-win1.3.40/NeoClash-1.2.62.dmg)

## 更新说明与校验

[macOS 1.2.62 发布说明](https://github.com/niujt/NeoClash-Releases/releases/tag/neoclash-v1.2.62-win1.3.40) · [macOS 对应 SHA256SUMS.txt](https://github.com/niujt/NeoClash-Releases/releases/download/neoclash-v1.2.62-win1.3.40/SHA256SUMS.txt) · [所有版本](https://github.com/niujt/NeoClash-Releases/releases) · [客户端源码](https://github.com/niujt/NeoClash)

[Windows 1.3.53 发布说明](https://github.com/niujt/NeoClash-Releases/releases/tag/windows-native-v1.3.53) · [Windows SHA256SUMS.txt](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.53/SHA256SUMS.txt)

Windows 双架构 CI 验证了 WPF 界面、真实内核、系统代理恢复和安装升级卸载。

## 第三方组件

安装包内含 [sing-box](https://github.com/SagerNet/sing-box)，使用 GPL-3.0-or-later 许可证。Windows 内核为稳定版 1.14.3 的证书指纹修复版 `1.14.3-neoclash.1`，仅回移上游整张证书 SHA256 校验；许可证、补丁、构建信息与修改后的对应源码归档随包提供。macOS 同样使用证书指纹修复版内核。
