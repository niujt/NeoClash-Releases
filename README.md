# NeoClash 下载

基于 sing-box 的原生代理客户端。本仓库提供 Windows 和 macOS 安装包、版本说明与 SHA256 校验文件。

## Windows 原生版 · x64 1.3.30 / ARM64 1.3.27

| 电脑 | 安装包 | 完整目录 ZIP |
| --- | --- | --- |
| Windows 10/11 · Intel / AMD 64 位 · 1.3.30（.NET Framework 4.8+） | [下载 x64 Setup.exe](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.30/NeoClash-1.3.30-Windows-Native-x64-Setup.exe) | [x64 ZIP](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.30/NeoClash-1.3.30-Windows-Native-x64.zip) |
| Windows 11 ARM64 · 1.3.27（.NET Framework 4.8.1+） | [下载 ARM64 Setup.exe](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.27/NeoClash-1.3.27-Windows-Native-arm64-Setup.exe) | [ARM64 ZIP](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.27/NeoClash-1.3.27-Windows-Native-arm64.zip) |

正常退出托盘中的旧版，运行对应架构 Setup，覆盖安装到原目录；订阅和设置保留，完成后手动打开 NeoClash。也可在原生版“更新”中依次执行“检查更新 → 下载更新 → 覆盖更新并退出”，再手动打开。Electron 用户使用 Setup 迁移。

Windows x64 1.3.30 新增独立迷你窗口：托盘或节点页“更多 → 迷你窗口”，也可按 Ctrl+Alt+M；支持订阅筛选、搜索、置顶、连接/断开，关闭后继续后台运行。节点列表缓存分组、按变化更新，加入行内收藏、节点详情、测速进度和取消；订阅额度查询失败时保留上次快照。保留 AnyTLS 证书指纹严格校验和 Wi-Fi 切换恢复。

本次仅更新 x64。ARM64 继续提供 1.3.27，macOS 下载保持原公开版本。

保留可选 TUN 与企业 VPN 会话隔离。Windows EXE / Setup 未做 Authenticode 签名。TUN 和企业引擎的既有管理员授权要求不变；真实企业登录与业务访问仍需在目标电脑确认。

## macOS 1.2.11 · build 44 · Apple Silicon

需要 macOS 14 或更新版本，目前正式版支持系统代理，TUN 暂不支持。

[下载 NeoClash-1.2.11.dmg](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.18/NeoClash-1.2.11.dmg)

正常退出运行中的 NeoClash，打开 DMG，将 NeoClash.app 安装到“应用程序”。本版包含动态节点 DNS、连接失败重试、测速有效期、近期节点分组和双状态界面，以及慢订阅刷新时限调整。使用 Apple Development 开发签名，未完成 Developer ID 签名与 Apple 公证。

Intel Mac 暂无本次更新包；[历史 Intel 1.1.24](https://github.com/niujt/NeoClash-Releases/releases/download/v1.1.24/NeoClash-1.1.24-Intel.dmg) 与当前 Apple Silicon 版版本不同，请按芯片选择。

## 更新说明与校验

[本次完整更新说明与验证记录](https://github.com/niujt/NeoClash-Releases/releases/tag/windows-native-v1.3.30) · [SHA256SUMS.txt](https://github.com/niujt/NeoClash-Releases/releases/download/windows-native-v1.3.30/SHA256SUMS.txt) · [所有版本](https://github.com/niujt/NeoClash-Releases/releases) · [客户端源码](https://github.com/niujt/NeoClash)

x64 1.3.30 的真实内核、更新、迷你窗口/完整界面与安装流程按目标平台 CI 校验，附件使用通过该次 CI 的产物，详细结果见本次 Release。真实订阅已完成 50 节点解析与配置检查，不代表全部真实节点代理连通。ARM64 的验证记录见 [1.3.27 Release](https://github.com/niujt/NeoClash-Releases/releases/tag/windows-native-v1.3.27)。

## 第三方组件

安装包内含 [sing-box](https://github.com/SagerNet/sing-box)，使用 GPL-3.0-or-later 许可证。Windows 内核为稳定版 1.14.3 的证书指纹修复版 `1.14.3-neoclash.1`，仅回移上游整张证书 SHA256 校验；许可证、补丁、构建信息与修改后的对应源码归档随包提供。macOS 内核仍为 1.14.0。
