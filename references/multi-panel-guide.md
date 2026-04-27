# 🖼️ S11 多图拼版指南 (Multi-Panel Guide)

**版本**: v1.0 (2026-04-27)

---

## 📌 概述

S11 场景用于生成多帧拼合、网格布局、对比图等需要在一个画面中展示多个视角/状态的场景。参考 GPT-Image-2 社区中的 3x3 网格、拼版海报等优秀案例。

**核心特点**:
- 一个 prompt 生成多帧拼合图
- 每个子帧的主体（人物/角色）必须 100% 一致
- 子帧之间通过姿态、角度、表情变化展现多样性

---

## 📐 拼版布局类型

| 类型 | 描述 | 适用场景 | 画幅建议 |
|------|------|---------|---------|
| 3x3 网格 | 九宫格，3行3列 | 角色摄影集、多角度展示 | 9:16 (竖版长图) |
| 2x2 四宫格 | 四格拼版 | 对比图、状态变化 | 1:1 或 4:3 |
| 左右对比 | 两图并排 | Before/After、不同风格对比 | 16:9 |
| 上下对比 | 两图上下排列 | 日夜对比、表情变化 | 9:16 |
| 电影胶片条 | 横向多帧排列 | 时间序列、动作分解 | 21:9 超宽 |

---

## 🔧 Prompt 结构模板

### 3x3 网格（最常用）

```
9:16 vertical — [主题描述]，3x3 grid collage (nine images forming a [系列描述])

**主体一致性声明**:
Same person across all nine frames, 100% consistency in facial features, proportions, hairstyle, and identity.

**子帧描述**（逐帧描述姿态/角度/表情）:
- Top left: [姿态1]
- Top center: [姿态2]
- Top right: [姿态3]
- Middle left: [姿态4]
- Center: [姿态5]
- Middle right: [姿态6]
- Bottom left: [姿态7]
- Bottom center: [姿态8]
- Bottom right: [姿态9]

**统一参数**:
- 服装: [统一服装描述]
- 发型: [统一发型描述]
- 背景: [统一背景]
- 光位: [统一光位]
- 色温: 5500K 中性光

**画质词**: ultra-realistic, 8K detail, subtle film grain
--ar 9:16
```

### 左右对比

```
16:9 horizontal — split-screen comparison showing [对比主题]

Left side: [左图描述]
Right side: [右图描述]

Both sides feature the same [主体], identical styling and features.
--ar 16:9
```

---

## ⚙️ 技术参数铁律

### 一致性锁定参数（子帧间必须一致）
| 参数 | 要求 |
|------|------|
| 面部特征 | 100% 一致（同一人） |
| 发型 | 完全一致 |
| 服装 | 完全一致 |
| 背景 | 统一环境 |
| 色温 | 5500K 中性光 |
| 光位 | 统一光位 |

### 允许变化参数（子帧间可以不同）
| 参数 | 变化范围 |
|------|---------|
| 拍摄方向 | 正面/侧面/斜侧/背面 |
| 姿态 | 站立/坐姿/侧身/转身等 |
| 表情 | 微笑/凝视/沉思等 |
| 手部动作 | 自然变化 |

---

## 📝 夏导引擎 10 维度适配

S11 场景的 10 维度参数填写规则：

| 维度 | S11 特殊处理 |
|------|-------------|
| 景别 | 指定为"[拼版类型]"，如"3x3 网格" |
| 拍摄高度 | 各子帧分别指定，或统一为"平拍" |
| 拍摄方向 | 各子帧不同，在提示词中逐帧描述 |
| 焦段 | 统一 50mm（确保各子帧视角一致） |
| 光位 | 统一光位（推荐正面平光或侧顺光） |
| 光比 | 1:1~2:1 柔和 |
| 主体 | 描述主体 + 强调一致性声明 |
| 环境 | 统一背景 |
| 色温 | 5500K / 5500K |
| 氛围 | 系列感、摄影集感、收藏感 |

---

## 🆕 GPT-Image-2 优秀案例转换参考

以下案例来自 awesome-gpt-image-2-prompts 仓库，已适配为 Midjourney 格式：

### 案例 1：Korean Idol 3x3 Grid Portrait

**原始场景**: K-pop 偶像摄影集九宫格
**转换后提示词**:
```
9:16 vertical — Korean idol portrait photoshoot series, 3x3 grid collage (nine frames)
Same young Korean female idol across all frames, 100% consistent facial features, proportions, hairstyle
Natural ultra-realistic skin texture, no retouching, clean minimal makeup, soft glow
Hair: long voluminous dark hair, slightly tousled, consistent across all frames
Outfit: white shirt + short bottoms, youthful clean styling, same across all frames
Setting: minimal studio, plain wall, soft window light, clean background
Lighting: soft diffused natural light, gentle highlights, low contrast, slightly airy tones
--ar 9:16
```

### 案例 2：Before/After 对比图

**原始场景**: 角色变身前后对比
**转换后提示词**:
```
16:9 horizontal — split-screen comparison portrait
Left side: [日常状态描述], casual clothing, natural lighting, relaxed expression
Right side: [华丽状态描述], elaborate costume, dramatic lighting, confident expression
Same person in both halves, identical facial features, before and after transformation
Cinematic lighting, ultra-realistic, 8K detail
--ar 16:9
```

---

## 🚫 常见错误

1. **忘记一致性声明** → 各子帧人物长相不同
2. **子帧描述不够差异化** → 九宫格看起来像复制粘贴
3. **没有统一服装/发型** → AI 会随机改变
4. **画幅比例不对** → 3x3 网格必须用 9:16 竖版
