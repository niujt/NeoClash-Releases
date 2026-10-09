# NeoClash 下载

基于 sing-box 的原生 macOS 代理客户端。此公开仓库提供安装包、版本说明及完整性校验文件。

## 当前版本：1.1.24（build 25）

需要 macOS 14 或更高版本。请选择与 Mac 芯片匹配的安装包：

| 芯片 | 安装包 |
| --- | --- |
| Apple Silicon（M 系列，arm64） | [NeoClash-1.1.24.dmg](https://github.com/niujt/NeoClash-Releases/releases/download/v1.1.24/NeoClash-1.1.24.dmg) |
| Intel（x86_64） | [NeoClash-1.1.24-Intel.dmg](https://github.com/niujt/NeoClash-Releases/releases/download/v1.1.24/NeoClash-1.1.24-Intel.dmg) |

[版本说明及校验文件](https://github.com/niujt/NeoClash-Releases/releases/tag/v1.1.24) · [所有版本](https://github.com/niujt/NeoClash-Releases/releases)

打开 DMG，先退出运行中的 NeoClash，再双击「安装并修复打开问题.command」。脚本验证应用后自动安装、备份旧版本，并仅处理 NeoClash 的下载隔离标记。两个安装包是同一应用的不同架构版本，请安装其中一个。

如果脚本本身被 macOS 拦截：打开「终端」，输入 bash 和一个空格，把 .command 文件拖入终端后按回车。详细步骤见包内「安装说明.txt」。只运行本仓库官方 Release 提供的文件；脚本不会关闭系统全局安全保护，也不需要管理员密码。

## 本版更新

- DMG 新增中文安装修复脚本及说明，保留旧版本备份，失败时回滚。
- 菜单栏采用紧凑快捷面板，节点选择收进菜单。
- TCP 与完整代理耗时分别显示，保留绿色与红色提示。
- 修复订阅刷新后的节点勾选及重复待连接提示。
- 退出时异步恢复系统代理并停止内核；恢复失败会取消退出并提示修复。
- 关闭主窗口后继续后台运行；详细流量统计位于主窗口。

## 验证与支持范围

60 项单元测试通过。两个安装包完成干净 Release 构建、架构及签名验证、资源检查和 DMG 完整性校验。

当前使用开发签名，尚未完成 Developer ID 签名与 Apple 公证。当前仅支持系统代理，TUN 暂不支持。修复脚本自身仍可能被 macOS 拦截；完整双击安装与 Intel 真机运行尚未验收。

## 第三方组件

安装包内含 [sing-box](https://github.com/SagerNet/sing-box)，使用 GPL-3.0-or-later 许可证。其许可证随内核一起放在应用 Resources 中；上游源代码及构建说明见官方仓库。
