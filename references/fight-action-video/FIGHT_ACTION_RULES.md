# 🥊 打戏/动作视频提示词规则（导演实战版）

> 基于真人动画导演培训总结提炼，2026-04-30
> 适用于 AI 视频生成（Seedance/可灵/Runway 等）

---

## 🔴 五大致命问题（生成前必检）

| 问题 | 表现 | 修复方式 |
|------|------|----------|
| 没有速度感 | 动作软绵绵像慢动作 | 必加标签 `高速运动` + 动态模糊描述 |
| 画面没有冲击感 | 镜头太平、构图无张力 | 必加标签 `高速运镜跟随` + 低角度/仰拍 |
| 站得太近 | 角色之间距离不合理 | 描述中明确站位距离（3-5米交战区） |
| 瞬移/穿帮 | 人物突然跳位 | 必加标签 `连续动作` + 明确位移轨迹 |
| **人和场景隔开** | 角色像贴在背景上（最严重） | 必加标签 `角色融入场景` + 光影交互描述 |

---

## 🎭 表情规则（加班最多的原因）

### 核心原则
**战斗中绝不允许"死脸"——从头到尾一个表情**

### 表情对照表
| 战斗状态 | 表情要求 | 提示词示例 |
|---------|---------|-----------|
| 攻击中 | 咬牙切齿/怒吼/专注 | `fierce expression, gritting teeth, intense focus` |
| 防御中 | 痛苦/吃力/皱眉 | `strained expression, grimacing, defensive posture` |
| 实力碾压 | 嘴角微笑/从容 | `slight confident smirk, relaxed demeanor` |
| 受击瞬间 | 痛苦/惊讶/后退 | `shocked expression, wincing from impact` |
| 胜利/收招 | 喘息/放松/得意 | `catching breath, triumphant look` |

### 提示词强制格式
```
[角色描述], [表情变化描述], [动作描述]
```
❌ 错误：`a girl in hanfu fighting`（无表情）
✅ 正确：`a girl in hanfu with fierce determined expression, teeth clenched, swinging her sword with full force`

---

## 📷 镜头/运镜规则

### 禁用项
| 规则 | 说明 |
|------|------|
| ❌ 禁用推镜头 | 一镜到底给观众感觉很假 |
| ❌ 禁止一镜到底 | 15秒镜头必须切至少3个镜头（正反打除外） |
| ❌ 前3个固定镜头不运镜 | 先用固定镜头建立空间感 |
| ❌ 对话时乱旋转运镜 | 对话用近景↔特写切换，不要360°旋转 |

### 必加标签（三选一或多选）
| 标签 | 适用场景 | 提示词关键词 |
|------|---------|-------------|
| **高速运镜跟随** | 追逐/连招/高速对打 | `high-speed camera tracking, dynamic motion blur` |
| **环绕运镜** | 对峙/蓄力/对拼瞬间 | `orbital camera movement, 180-degree arc shot` |
| **快速切换镜头** | 连击/多角色混战 | `rapid shot cuts, quick cuts between angles` |

### 镜头切换模板（15秒标准）
```
镜头1（0-3s）：全景建立场景 → 固定镜头
镜头2（3-8s）：中景打斗 → 高速运镜跟随
镜头3（8-12s）：特写表情/武器 → 快速切换
镜头4（12-15s）：全景收招/结果 → 固定镜头
```

---

## 🚀 打戏提示词公式

### 标准结构
```
[场景描述 + 角色站位], [角色A描述 + 表情 + 动作], [角色B描述 + 表情 + 动作],
[镜头运动：高速运镜跟随/环绕/快切],
[速度感关键词：motion blur, impact frames, dynamic camera],
[表情关键词：fierce expression, determined look],
[场景交互关键词：dust kicking up, debris flying, lighting interaction]
```

### 完整示例
```
Ancient Chinese courtyard at dusk, two martial artists facing each other 5 meters apart, 
Character A: young woman in light cyan Tang dynasty hanfu with fierce determined expression, teeth clenched, drawing her sword from the scabbard,
Character B: tall warrior in black armor with confident smirk, raising his broadsword,
high-speed camera tracking shot following Character A's charge, dynamic motion blur, 
sparks flying as blades clash, dust kicking up from footwork,
rapid cuts between close-ups of their faces and wide shots of the clash,
cinematic lighting with volumetric light beams, photorealistic, 8K
```

---

## ⚠️ AI模型避坑指南

### 吉梦（Jimeng）常见问题
| 问题 | 原因 | 解决方案 |
|------|------|----------|
| 生成慢镜头/拖沓 | 模型偷懒 | 出现"拉稀感"直接换模型/重新生成 |
| 表情不变 | 模型默认中性表情 | 提示词前30%必须写表情 |
| 人物浮空 | 场景融合不足 | 加 `grounded stance, feet firmly on ground` |

### 模型选择建议
| 场景 | 推荐模型 |
|------|---------|
| 高速打斗 | Seedance 2.0 / 可灵 1.6 Pro |
| 表情特写 | Seedance 2.0 |
| 场景融合 | 可灵 1.6 Pro |
| 快速切换 | Runway Gen-3 Alpha |

---

## ✅ 生成前自检清单

- [ ] 是否加了高速运动标签？
- [ ] 是否有表情变化描述？
- [ ] 是否切了至少3个镜头（15秒内）？
- [ ] 角色是否融入场景（非浮空/贴图感）？
- [ ] 是否有速度感/冲击感关键词？
- [ ] 是否避免了推镜头/一镜到底？
- [ ] 站位距离是否合理（非贴脸）？

**7项全勾 ✅ 才可提交生成**
