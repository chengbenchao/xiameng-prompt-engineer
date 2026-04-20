# 🎬 夏导提示词生成引擎 (XiaMeng Prompt Engineer)

> **让 AI 像导演一样思考。**
> 基于影视工业级 SOP 的 AI 绘画提示词生成 Skill。

[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-1.0.0-blue.svg)](https://github.com/)

## ✨ 核心特性

- **🧠 10 维度结构化思维**：摒弃废话，精准控制景别、光位、焦段、色温。
- **🛡️ 铁律参数库**：内置严格的色温/焦段对照表，防止 AI 幻觉瞎编参数。
- **⚙️ SOP 自动化工作流**：需求翻译 -> 查表 -> 填空 -> 渲染 -> 自检，步步为营。
- **🚀 极速模式 (Fast Track)**：默认只输出参数表与提示词，高效出图。
- **📚 内置标杆库**：包含 S1-S8 经典场景的高质量提示词范文，支持 Few-Shot 学习。

## 🚀 安装与使用

### 1. 安装
将本仓库（或 `skills/xiameng-prompt-engineer` 文件夹）复制到你的 Agent 工作区的 `skills/` 目录下：

```bash
cp -r xiameng-prompt-engineer /path/to/your/agent/workspace/skills/
```

### 2. 触发方式
在对话中描述你的画面需求，例如：
> "帮我写一个 22 岁东方男性，坚毅性格，在 S3 宗门场景的提示词。"

### 3. 模式切换
- **极速模式（默认）**：仅展示核心参数与结果。
- **标准模式**：在指令前加上“详细分析”，获取完整的导演思维推导与评分报告。

## ⚙️ 技术架构

本 Skill 由以下核心组件构成：

- `SKILL.md`: 定义了 Agent 必须遵循的 5 步工作流 (SOP) 和红线自检逻辑。
- `references/core-rules.md`: 存储硬性约束参数（色温表、焦段表）。
- `references/prompt-database/`: 存储各场景的高质量提示词示例 (S1-S8)。

## ⚠️ 使用须知 (Best Practices)

1. **模型要求**：建议使用 **GPT-4o**、**Claude 3.5 Sonnet** 或 **Qwen-Max** 等逻辑能力强的模型，以确保 Agent 严格执行查表和自检步骤。
2. **参考图一致性**：生成的提示词中会包含“参考图一”、“参考图二”等占位符。在实际 AI 绘画工具（如 Midjourney/Stable Diffusion）中使用时，请配合垫图（Image Prompt）或 ControlNet 使用以保证角色一致性。
3. **参数微调**：`references/core-rules.md` 中的参数是基于《仙门之下》项目总结的。你可以编辑该文件，将其替换为你自己项目的场景参数。

## 📄 许可协议

本项目遵循 MIT 协议开源。
