# NeoClash 下载

基于 sing-box 的原生代理客户端。本仓库提供 Windows 和 macOS 安装包、版本说明与 SHA256 校验文件。

## Windows · x64 / ARM64 1.3.41

| 电脑 | 安装包 | 完整目录 ZIP |
| --- | --- | --- |
| Windows 10/11 · Intel / AMD 64 位 · 1.3.41（.NET Framework 4.8+） | [下载 x64 Setup.exe](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.41/NeoClash-1.3.41-Windows-Native-x64-Setup.exe) | [x64 ZIP](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.41/NeoClash-1.3.41-Windows-Native-x64.zip) |
| Windows 11 ARM64 · 1.3.41（.NET Framework 4.8.1+） | [下载 ARM64 Setup.exe](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.41/NeoClash-1.3.41-Windows-Native-arm64-Setup.exe) | [ARM64 ZIP](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.41/NeoClash-1.3.41-Windows-Native-arm64.zip) |

正常退出托盘中的旧版，运行对应架构 Setup，覆盖安装到原目录；订阅和设置保留，完成后手动打开 NeoClash。也可在应用的“更新”中依次执行“检查更新 → 下载更新 → 覆盖更新并退出”，再手动打开。Electron 用户使用 Setup 迁移。

1.3.41 将 Windows 主窗口和迷你窗口迁移到 WPF + WPF UI。节点页集中搜索、筛选、排序和测速，连接后的断开按钮使用饱和蓝色。

本次更新覆盖 Windows x64 与 ARM64。

保留可选 TUN 与企业 VPN 会话隔离。Windows EXE / Setup 未做 Authenticode 签名。TUN 和企业引擎的既有管理员授权要求不变；真实企业登录与业务访问仍需在目标电脑确认。

## macOS 1.2.62 · build 95 · Apple Silicon

需要 macOS 14 或更新版本，目前正式版支持系统代理，TUN 暂不支持。

[下载 NeoClash-1.2.62.dmg](https://github.com/niujt/NeoClash-Releases/releases/download/neoclash-v1.2.62-win1.3.40/NeoClash-1.2.62.dmg)

正常退出运行中的 NeoClash，打开 DMG，将 NeoClash.app 安装到“应用程序”。火箭图标随系统深浅外观切换。ChatGPT 网页检测单独显示超时与 TLS 握手失败。使用 Apple Development 开发签名，未完成 Developer ID 签名与 Apple 公证。

Intel Mac 暂无本次更新包；[历史 Intel 1.1.24](https://github.com/niujt/NeoClash-Releases/releases/download/v1.1.24/NeoClash-1.1.24-Intel.dmg) 与当前 Apple Silicon 版版本不同，请按芯片选择。

## 更新说明与校验

[macOS 1.2.62 发布说明](https://github.com/niujt/NeoClash-Releases/releases/tag/neoclash-v1.2.62-win1.3.40) · [macOS 对应 SHA256SUMS.txt](https://github.com/niujt/NeoClash-Releases/releases/download/neoclash-v1.2.62-win1.3.40/SHA256SUMS.txt) · [所有版本](https://github.com/niujt/NeoClash-Releases/releases) · [客户端源码](https://github.com/niujt/NeoClash)

[Windows 1.3.41 发布说明](https://github.com/niujt/NeoClash-Releases/releases/tag/windows-native-v1.3.41) · [Windows SHA256SUMS.txt](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.41/SHA256SUMS.txt)

Windows 双架构 CI 验证了 WPF 界面、真实内核、系统代理恢复和安装升级卸载。

## 第三方组件

安装包内含 [sing-box](https://github.com/SagerNet/sing-box)，使用 GPL-3.0-or-later 许可证。Windows 内核为稳定版 1.14.3 的证书指纹修复版 `1.14.3-neoclash.1`，仅回移上游整张证书 SHA256 校验；许可证、补丁、构建信息与修改后的对应源码归档随包提供。macOS 同样使用证书指纹修复版内核。
