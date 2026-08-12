[README.md](https://github.com/user-attachments/files/30971803/README.md)
# Qtalis NavLink

**GNSS receiver communication, monitoring, evaluation, and correction-data tool for Windows.**

[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-1473E6)](https://www.microsoft.com/windows)
[![Version](https://img.shields.io/badge/version-1.2.1-0E7888)](https://github.com/chengjinquan1210-hash/Qtalis_Navlink/releases)
[![Website](https://img.shields.io/badge/Qtalis-Official%20Website-16835B)](https://www.qtalisgnss.com/)

Qtalis NavLink 是一款面向 GNSS 接收机、模块和数据电台的 Windows 桌面工具，覆盖设备连接、命令交互、原始数据可靠保存、卫星信号监测、定位精度评估、NTRIP 差分服务、RINEX 转换与观测质量分析等常见工作流程。

Qtalis NavLink is a Windows desktop application for GNSS receiver communication, raw-data capture, satellite monitoring, positioning evaluation, NTRIP correction services, RINEX conversion, and observation-quality analysis.

## 下载 / Download

请从仓库的 [Releases](https://github.com/chengjinquan1210-hash/Qtalis_Navlink/releases) 页面下载最新的 Windows x64 ZIP 包。

Download the latest Windows x64 ZIP package from [Releases](https://github.com/chengjinquan1210-hash/Qtalis_Navlink/releases).

1. 下载 `QtalisNavLink-vX.Y.Z-win-x64.zip`。
2. 将 ZIP 完整解压到一个可写目录。
3. 运行 `QtalisNavLink.exe`。
4. 请勿只复制 EXE；运行所需 DLL、`Updater` 和 `Tools` 目录必须保留。

> Windows may show a SmartScreen warning for an unsigned build. Verify that the package was downloaded from this repository before running it.

## 主要功能 / Features

### 数据终端

- 支持两个独立设备，每个设备均可使用串口或 TCP。
- ASCII/HEX 接收与发送、时间戳、自动滚动和定时发送。
- 常用命令、NMEA 与 SinoGNSS 自定义日志快捷配置。
- 高速原始数据保存，显示写入队列、串口错误和保存完整性状态。
- 保存期间可暂停解析，优先保证高速二进制数据完整记录。

### 卫星与定位

- 支持 GPS、BDS、GLONASS、Galileo、QZSS、SBAS 和 NavIC。
- 解析 NMEA，以及 ComNav M925、Unicore SATSINFOB 和 u-blox 原始卫星信息。
- 显示多频 C/N0 柱状图、完整频点表格和天空图。
- 在线地图支持高德地图和 OpenStreetMap。
- 解析 BESTPOS、GPGGA、GPVTG、HEADINGA 和 HEADING2A。

### 定位评估

- ENU 位置散点、误差时间序列和航向可视化。
- 支持双设备对比、评估阈值和结果导出。
- 可导出包含统计表、水平散点图和误差曲线的 HTML 报告。

### 差分服务

- 内置 NTRIP Client，可在未连接接收机时独立监控和保存 RTCM。
- 支持获取挂载点、VRS 手动坐标 GGA 和双设备 RTCM 转发。
- 实时解码 RTCM 消息类型并统计 CRC、逐秒数据覆盖和接收完整率。
- 支持保存、重命名和删除 NTRIP 快捷配置。

### RINEX 与日志

- 日志录制、回放、倍速控制和原始数据导出。
- 集成 RINEX 转换工具。
- 统计观测时段、采样率、历元完整率、周跳事件、MP1/MP2 RMS 和各系统 C/N0。
- 按卫星显示多频 C/N0 时间序列。

### 其他

- 中英文界面切换。
- 内置常用工作模式、电台配置和 OEM 指令参考。
- 提供资料与固件目录、产品目录和官方资源入口。
- 支持 GitHub OTA 自动更新。

## 快速开始 / Quick Start

1. 连接 GNSS 设备，并确认 Windows 已识别串口或设备 TCP 地址。
2. 打开“数据终端”，选择端口和波特率，点击“连接设备 1”。
3. 在终端查看输出，或使用快捷指令配置接收机消息。
4. 打开“卫星信号”查看多系统、多频点 C/N0 与天空图。
5. 打开“定位状态”或“定位评估”查看实时位置和精度。
6. 使用“差分服务”连接 NTRIP caster，并选择 RTCM 转发目标。

详细说明参见软件仓库中的操作手册：
[Qtalis NavLink 操作手册](docs/Qtalis_NavLink_操作手册_v1.0.7.md)

## 自动更新 / OTA Updates

Qtalis NavLink 会在启动后静默检查更新，并在运行期间每 6 小时检查一次。发现新版本后，用户可确认下载安装：

1. 下载 GitHub Release ZIP。
2. 校验 SHA-256。
3. 关闭主程序并由独立更新器替换文件。
4. 更新失败时恢复旧文件。
5. 更新成功后自动重启。

更新过程不会修改用户保存的 GNSS 日志、RINEX 文件或导出报告。

## 系统要求 / Requirements

- Windows 10 或 Windows 11，x64
- 建议分辨率：1366 × 768 或更高
- 串口设备需要正确安装对应 USB/串口驱动
- 地图、NTRIP、资料链接和软件更新需要网络连接
- 当前轻量发布包需要 .NET 8 Desktop Runtime

## 发布维护 / Release Maintenance

维护者发布新版本时：

1. 生成完整的 Windows x64 发布目录。
2. 将目录内容直接压缩为 `QtalisNavLink-vX.Y.Z-win-x64.zip`，ZIP 根目录必须包含 `QtalisNavLink.exe`。
3. 在 GitHub 创建同版本 Tag 和 Release，并上传 ZIP。
4. 计算 ZIP 的 SHA-256。
5. 更新仓库根目录的 `update.json`，填写版本、Release 直链、SHA-256 和更新说明。
6. 上传清单前先确认 Release 文件可以公开下载。

清单格式参见 [update-manifest.example.json](docs/update-manifest.example.json)，完整流程参见 [OTA 发布说明](docs/Qtalis_NavLink_OTA发布说明.md)。

## 支持与资源 / Support

- [Qtalis Official Website](https://www.qtalisgnss.com/)
- [Qtalis Resource Hub](https://www.qtalisgnss.com/pages/resource-hub)
- [Qtalis Forum](https://www.qtalisgnss.com/community/forum)
- [GitHub Issues](https://github.com/chengjinquan1210-hash/Qtalis_Navlink/issues)

## Notice

Qtalis NavLink is intended for GNSS receiver integration, testing, monitoring, and engineering evaluation. Verify receiver commands, firmware compatibility, radio parameters, and correction-service credentials before use in production environments.

Copyright © Qtalis. All rights reserved.
