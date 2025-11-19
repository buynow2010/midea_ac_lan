# Midea AC LAN（完整汉化版）

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/hacs/integration)
[![Version](https://img.shields.io/badge/version-0.6.10-blue.svg)](https://github.com/buynow2010/midea_ac_lan)
[![Home Assistant](https://img.shields.io/badge/Home%20Assistant-2023.8%2B-green.svg)](https://www.home-assistant.io/)

通过局域网控制美的 M-Smart 智能家电，完整简体中文界面，支持空调外部温湿度传感器。

基于官方项目 [wuwentao/midea_ac_lan](https://github.com/wuwentao/midea_ac_lan) 进行完整汉化和功能增强。

## 快速安装

[![添加到 HACS](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=buynow2010&repository=midea_ac_lan&category=integration)

## 特色功能

### 完整简体中文化
- 35 种设备类型名称
- 420+ 个实体名称
- 所有配置界面
- 72 个状态值翻译

### 空调外部传感器
- 外部温度/湿度传感器替换内置传感器
- 实时监听状态变化
- 智能自动回退
- 摆动功能禁用选项
- HomeKit Bridge 兼容

### 核心功能
- 自动发现设备
- 扩展传感器和开关
- 实时状态同步
- 可视化配置界面

## 支持的品牌

美的、Carrier、Toshiba、Comfee、Electrolux、Ariston、小天鹅、华凌、COLMO 等。

## 支持的设备

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

- Home Assistant 2023.8.0+
- 设备与 Home Assistant 在同一局域网
- 建议为设备设置静态 IP 地址

## 安装

### 通过 HACS（推荐）

1. 在 HACS 中点击右上角菜单 → 自定义存储库
2. 添加仓库地址：`https://github.com/buynow2010/midea_ac_lan`
3. 类别选择：Integration
4. 搜索并安装 "Midea AC LAN"
5. 重启 Home Assistant

### 手动安装

1. 下载 [最新版本](https://github.com/buynow2010/midea_ac_lan/releases/latest)
2. 解压到 `custom_components/midea_ac_lan`
3. 重启 Home Assistant

## 添加设备

⚠️ **建议先在路由器中为设备设置静态 IP**

1. 在 Home Assistant 集成页面搜索 `Midea AC LAN`
2. 首次配置需要输入美的账号密码（获取设备 Token）
3. 选择自动发现或手动配置设备
4. 配置完成后可移除账号配置

## 配置

在 `设置 -> 设备与服务 -> Midea AC LAN -> 设备 -> 配置` 中：

- **IP 地址**：设备 IP 变化时重新设置
- **刷新间隔**：默认 30 秒
- **扩展传感器**：选择额外的传感器和开关实体

### 空调外部传感器（新增功能）

- **外部温度传感器**：替代内置温度传感器
- **外部湿度传感器**：替代内置湿度传感器  
- **禁用摆动功能**：完全隐藏摆动选项

外部传感器不可用时自动回退到内置传感器，HomeKit Bridge 会显示外部传感器值。

## 故障排除

**界面显示英文**：重新加载集成或清除浏览器缓存

**设备无法发现**：确认设备和 HA 在同一子网

**外部传感器不工作**：检查传感器实体 ID 和状态值

## 许可证

MIT License - 详见 [LICENSE](LICENSE)

## 致谢

基于 [wuwentao/midea_ac_lan](https://github.com/wuwentao/midea_ac_lan) 官方项目
