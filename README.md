# Midea AC LAN（完整汉化版）

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/hacs/integration)
[![Version](https://img.shields.io/badge/version-0.6.10-blue.svg)](https://github.com/buynow2010/midea_ac_lan)
[![Home Assistant](https://img.shields.io/badge/Home%20Assistant-2023.8%2B-green.svg)](https://www.home-assistant.io/)

通过局域网控制美的 M-Smart 智能家电（空调、风扇、热水器、洗衣机等），完整简体中文界面，支持空调外部温湿度传感器。

本仓库基于官方项目进行完整汉化和功能增强，专为中文用户优化。

**官方仓库**: [wuwentao/midea_ac_lan](https://github.com/wuwentao/midea_ac_lan)

## 🚀 快速开始

<table>
<tr>
<td align="center">
<a href="https://my.home-assistant.io/redirect/hacs_repository/?owner=buynow2010&repository=midea_ac_lan&category=integration">
<img src="https://my.home-assistant.io/badges/hacs_repository.svg" alt="添加HACS仓库" />
</a>
<br />
<strong>添加到 HACS</strong>
</td>
<td align="center">
<img src="https://img.shields.io/badge/点击上方-快速安装-brightgreen?style=flat-square" alt="快速安装" />
<br />
<strong>一键安装</strong>
</td>
</tr>
</table>

## ✨ 本仓库特色

### 🇨🇳 完整简体中文化
- ✅ **设备类型名称**（35 种设备类型）
- ✅ **实体名称**（420+ 个实体）
- ✅ **配置界面**（所有配置选项）
- ✅ **状态翻译**（72 个状态值）
- ✅ **错误消息**（所有提示信息）

### 🌡️ 空调外部传感器功能
- ✅ **外部温度传感器** - 使用其他温度传感器替代空调内置传感器
- ✅ **外部湿度传感器** - 使用其他湿度传感器替代空调内置传感器
- ✅ **实时监听** - 自动监听传感器状态变化并实时更新
- ✅ **智能回退** - 外部传感器不可用时自动回退到内置传感器
- ✅ **摆动控制** - 可选择完全禁用空调摆动功能

**应用场景**：
- 空调内置传感器不准确
- 需要使用房间中央的独立温湿度传感器
- 通过 HomeKit Bridge 暴露到 HomeKit（显示外部传感器值）

## 功能特性

### 🎛️ 核心功能
- 🔍 **自动发现设备** - 基于 Home Assistant 配置流 UI 自动发现和配置设备
- 📊 **扩展传感器和开关** - 可选择添加额外的传感器和开关实体
- 🔄 **实时状态同步** - 通过长连接 TCP 实时同步设备状态
- 🎨 **可视化编辑器** - 直观的界面选择器（温度/湿度传感器）

### 🏠 支持的品牌

<table>
<tr>
<td><img src="brands/midea.png" alt="Midea" height="40"></td>
<td><img src="brands/carrier.png" alt="Carrier" height="40"></td>
<td><img src="brands/toshiba.png" alt="Toshiba" height="40"></td>
<td><img src="brands/comfee.png" alt="Comfee" height="40"></td>
</tr>
<tr>
<td><img src="brands/electrolux.png" alt="Electrolux" height="40"></td>
<td><img src="brands/ariston.png" alt="Ariston" height="40"></td>
<td><img src="brands/beverly.png" alt="Beverly" height="40"></td>
<td><img src="brands/colmo.png" alt="COLMO" height="40"></td>
</tr>
</table>

以及更多品牌（小天鹅、华凌、Rotenso、Vandelo等）。

### 🔌 支持的设备类型

| 类型 | 设备名称 | 文档 | 类型 | 设备名称 | 文档 |
|------|---------|------|------|---------|------|
| AC | 空调 | [AC.md](doc/AC.md) | A1 | 除湿机 | [A1.md](doc/A1.md) |
| CA | 冰箱 | [CA.md](doc/CA.md) | DA | 波轮洗衣机 | [DA.md](doc/DA.md) |
| DB | 滚筒洗衣机 | [DB.md](doc/DB.md) | DC | 干衣机 | [DC.md](doc/DC.md) |
| E1 | 洗碗机 | [E1.md](doc/E1.md) | E2 | 电热水器 | [E2.md](doc/E2.md) |
| E3 | 燃气热水器 | [E3.md](doc/E3.md) | FA | 风扇 | [FA.md](doc/FA.md) |
| FB | 电加热器 | [FB.md](doc/FB.md) | FC | 空气净化器 | [FC.md](doc/FC.md) |
| FD | 加湿器 | [FD.md](doc/FD.md) | B6 | 油烟机 | [B6.md](doc/B6.md) |
| EA | 电饭煲 | [EA.md](doc/EA.md) | EC | 电压力锅 | [EC.md](doc/EC.md) |
| ED | 饮水机 | [ED.md](doc/ED.md) | CE | 新风系统 | [CE.md](doc/CE.md) |

查看 [doc](doc) 目录获取完整设备列表和详细文档。

## 系统要求

### Home Assistant
- 版本：2023.8.0+
- 已配置网络和设备

### 网络要求
- Home Assistant 和设备必须在同一局域网
- 建议在路由器中为设备设置静态 IP 地址

## 安装方式

### 方法一：通过 HACS 安装（推荐）

[![添加HACS仓库](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=buynow2010&repository=midea_ac_lan&category=integration)

**一键安装（推荐）**：点击上方徽章，直接在 HACS 中添加此仓库

**手动添加**：
1. 确保已安装 [HACS](https://hacs.xyz/)
2. 在 HACS 中点击右上角菜单 → **自定义存储库**
3. 添加仓库地址：`https://github.com/buynow2010/midea_ac_lan`
4. 类别选择：**Integration**
5. 点击 **添加**
6. 在 HACS 中搜索 "**Midea AC LAN**"
7. 点击 **下载**
8. 重启 Home Assistant

### 方法二：使用脚本安装

在 HA 终端或 SSH 附加组件中运行：

```bash
wget -O - https://github.com/wuwentao/midea_ac_lan/raw/master/scripts/install.sh | ARCHIVE_TAG=latest bash -
```

### 方法三：手动安装

1. 下载 [最新版本](https://github.com/buynow2010/midea_ac_lan/releases/latest) 的 `midea_ac_lan.zip`
2. 解压到 Home Assistant 配置目录的 `custom_components/midea_ac_lan`
3. 重启 Home Assistant

## 添加设备

### ⚠️ 重要提示
**首先在路由器中为设备设置静态 IP 地址，避免 IP 变化导致连接失败。**

### 配置步骤

1. 安装完成后，在 Home Assistant 集成页面搜索 `Midea AC LAN`
2. 或点击：[![Configuration](https://my.home-assistant.io/badges/config_flow_start.svg)](https://my.home-assistant.io/redirect/config_flow_start?domain=midea_ac_lan)
3. 首次配置需要输入美的账号密码（用于获取设备 Token 和 Key）
4. 配置完成后可以移除账号配置而不影响设备使用

### 添加方式

#### 1. 自动发现（推荐）
- 组件会自动发现局域网内的美的设备
- 也可以指定网络范围（如 `192.168.1.255`）
- **要求设备与 Home Assistant 在同一子网**

#### 2. 手动配置
如果您已知设备信息，可以手动添加：
- 设备 ID
- 设备类型（参考上方支持的设备）
- IP 地址
- 端口（默认 6444）
- 协议版本
- Token
- Key

#### 3. 仅列出设备
列出网络中所有可发现的美的设备及其 ID、类型、序列号等信息。

## 设备配置

在 `设置 -> 设备与服务 -> Midea AC LAN -> 设备 -> 配置` 中可以进行以下配置：

### IP 地址
当设备 IP 变化时，可以在此重新设置。

### 刷新间隔
设置主动刷新设备状态的间隔（秒）：
- 默认：30 秒
- 0：不主动刷新（依赖设备主动通知）
- 建议：30 秒

**注意**：更短的刷新间隔可能增加功耗。

### 扩展传感器和开关
选择将设备属性转换为独立的传感器和开关实体。

### 空调专用配置（本仓库新增）

#### 外部温度传感器
选择一个温度传感器实体替代空调内置温度传感器：
- 使用实体选择器，自动筛选温度传感器
- 实时监听传感器状态变化
- 外部传感器不可用时自动回退到内置传感器
- HomeKit Bridge 会显示外部传感器的值

#### 外部湿度传感器
选择一个湿度传感器实体替代空调内置湿度传感器：
- 使用实体选择器，自动筛选湿度传感器
- 功能与外部温度传感器相同

#### 禁用摆动功能
勾选后，空调实体将完全不显示摆动模式选项：
- 未勾选：显示摆动模式（关闭/垂直/水平/双向）
- 勾选：完全移除摆动功能

**配置示例**：

```
设置 -> 设备与服务 -> Midea AC LAN -> 设备 -> 配置

IP 地址: 192.168.1.100
刷新间隔: 30
扩展传感器: [☑ 室内温度 ☑ 室内湿度]
━━━━━━━━━━━━━━━━━━━━━
外部温度传感器: [选择传感器 ▼]  ← 选择 sensor.living_room_temperature
外部湿度传感器: [选择传感器 ▼]  ← 选择 sensor.living_room_humidity
禁用摆动功能: [☐]
```

### 自定义配置
部分设备类型有专门的配置项，格式必须为 JSON：

```json
{ "refresh_interval": 15, "fan_speed": 100 }
```

参考各设备文档了解具体配置项。

## 调试与测试

详见 [调试与测试文档](doc/debug.md)

## 故障排除

### 设备无法发现
1. 确认设备和 Home Assistant 在同一子网
2. 检查设备网络连接是否正常
3. 尝试使用手动配置方式

### 配置界面显示英文
1. 重新加载集成：`配置 -> 集成 -> Midea AC LAN -> 重新加载`
2. 或重启 Home Assistant
3. 清除浏览器缓存（Ctrl+Shift+R 或 Cmd+Shift+R）

### 外部传感器不工作
1. 检查传感器实体 ID 是否正确
2. 确认传感器有有效的状态值
3. 查看 Home Assistant 日志是否有错误信息

### HomeKit 显示问题
HomeKit Bridge 会读取空调的 `current_temperature` 和 `current_humidity` 属性：
- 配置外部传感器后，HomeKit 显示外部传感器的值
- 外部传感器不可用时，自动显示内置传感器的值

## 更新日志

### v0.6.10-zh (当前版本)
- ✅ 完整简体中文化（设备类型、实体、界面、状态）
- ✅ 空调外部温度传感器支持
- ✅ 空调外部湿度传感器支持
- ✅ 空调摆动功能禁用选项
- ✅ 实体选择器界面优化
- ✅ HomeKit Bridge 完美兼容

## 贡献与支持

### 问题反馈
- [GitHub Issues](https://github.com/buynow2010/midea_ac_lan/issues)

### 讨论交流
- [GitHub Discussions](https://github.com/buynow2010/midea_ac_lan/discussions)
- [Discord Chat](https://discord.com/invite/ZWdd2fXndn)

## 友情链接

### 🏠 Home Assistant 中文网

[![Home Assistant 中文网](https://img.shields.io/badge/Home%20Assistant-中文网-blue?style=for-the-badge&logo=home-assistant)](https://www.hasscn.top)

[**Home Assistant 中文网 (hasscn.top)**](https://www.hasscn.top) - 最全面的免费 Home Assistant 中文站点，提供：
- 🚀 **Home Assistant OS 极速版** - 专为中国优化的加速版系统
- ⚡ **HACS 极速版** - 使用国内镜像加速插件下载
- 📚 **中文文档教程** - 详细的安装配置指南
- 💬 **社区支持** - 微信公众号：老王杂谈说

**特别适合国内用户使用，解决下载慢、连接困难等问题！**

## 许可证

MIT License - 详见 [LICENSE](LICENSE)

## 致谢

- [wuwentao/midea_ac_lan](https://github.com/wuwentao/midea_ac_lan) - 官方项目
- [georgezhao2010](https://github.com/georgezhao2010) - 原作者
- [Home Assistant](https://www.home-assistant.io/) - 开源智能家居平台
- [HACS](https://hacs.xyz/) - Home Assistant 社区商店

---

**如果本项目对你有帮助，欢迎 Star 支持！** ⭐
