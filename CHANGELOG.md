# 更新日志

## [v0.6.11] - 2025-11-20

### 重大改进
- **完整汉化滚筒洗衣机（DB）和干衣机（DC）的所有状态属性翻译**
  - program（程序）状态：从17个增加到**128个**完整翻译
  - status（状态）状态：从15个增加到**24个**完整翻译
  - 补充了temperature实体的名称翻译
- 更新manifest.json中的文档和问题跟踪链接，指向当前仓库
- 移除了冗余的requirements.txt文件（依赖已在manifest.json中定义）
- 验证了HACS配置的完整性

### 详细翻译内容

**program状态翻译（128个）**
包含所有滚筒洗衣机和干衣机的程序模式：
- 基础洗涤：棉麻、丝绸、羊毛、化纤、混合洗等
- 快速洗涤：快洗、快洗30分钟、快洗60分钟等
- 特殊护理：婴儿服、运动服、衬衫、内衣、羽绒服等
- 水洗系列：水洗混合(water_mixed_wash)、水洗棉、水洗化纤等
- 烘干模式：快烘、智能烘、低温烘、节能烘等
- 消毒护理：蒸汽消毒洗、除螨洗、防过敏、香薰等
- 其他功能：筒自洁、空气洗、浸泡、除湿等

**status状态翻译（24个）**
包含所有设备运行状态：
- 基础状态：待机(idle)、准备(standby)、开始(start)、暂停(pause)、结束(end)
- 运行状态：运行中(running)、已暂停(paused)、已完成(completed)
- 洗涤阶段：洗涤中(washing)、漂洗中(rinsing)、脱水中(spinning)、烘干中(drying)
- 预处理：预洗中(prewash)、浸泡中(soaking)、加热中(heating)、冷却中(cooling)
- 特殊状态：防皱结束(prevent_wrinkle_end)、延时(delay)、延时选择(delay_choosing)、延时暂停(delay_pause)
- 错误状态：错误(error)、故障(fault)、关闭(off)、开启(on)

**实体名称翻译**
滚筒洗衣机（DB）和干衣机（DC）的所有实体：
- 传感器：status、mode、progress、program、water_level、temperature、dehydration_speed、wash_time、detergent、softener、stains、dirty_degree、dryness_level、dry_temperature、intensity、material、water_box、door_warn、ai_switch、error_code、time_remaining
- 开关：power、start
