# 🥊 S44 东方科幻+仙侠融合战斗视频（参考图版）

> 标杆范文编号：SCIFI-FIGHT-002
> 模型：Seedance 2.0
> 时长：10秒
> 输入：3张参考图（角色/动作姿态/面部特写）
> 风格：东方科幻 + 仙侠融合

---

## 参考图上传

使用 `upload_file.py` 上传3张参考图到 LibTV OSS，获取 HTTPS 链接后在提示词中引用：
- 参考图1（角色站立）
- 参考图2（动态战斗姿态）
- 参考图3（面部特写）

---

## 完整提示词（英文 Seedance 2.0 图生视频）

```
Generate a 10-second cinematic action video using Seedance 2.0 with these 3 reference images:

Reference Image 1 (character): [上传后替换URL]
Reference Image 2 (action pose): [上传后替换URL]
Reference Image 3 (facial close-up): [上传后替换URL]

The character must maintain fierce battle expression throughout the entire video — gritting teeth during attacks, intense focused eyes, eyebrows furrowed, battle-ready look, absolutely no neutral face. She wears a light cyan Tang dynasty hanfu with flowing shawl and hair ornaments, wielding a glowing red energy long sword with intense energy trails and particle effects.

Scene: futuristic Eastern sci-fi aerial battlefield above sea of clouds, environment color temperature 5500K cool battlefield light, subject face color temperature 5000K warm sword light fill light, strong cold-warm contrast. Massive floating warships distributed 3-10 meters around character in combat distance, volumetric clouds弥漫, tight lighting interaction, character fully grounded in scene no floating feeling.

Storyboard (10s 10 shots, must cut shots, no single continuous shot):
0-1s: 24mm wide angle wide shot, swordswoman floating above clouds, full moon and warship fleet background, clothes and shawl fluttering, fierce expression
1-2s: 85mm close-up fast push, she dives accelerating, fierce eyes gritting teeth, leaving red sword light trail, motion blur
2-3s: 85mm close-up handheld, she charges toward camera, gritting teeth intense focused eyes, raising sword
3-4s: 24mm wide angle high-speed tracking, flies past first warship, horizontal slash cutting it in half with explosion, impact frames dust and debris flying
4-5s: 24mm wide angle, weaving through warship fleet, continuous slashes, multiple ships exploding in chain reaction, rapid cuts
5-6s: orbital camera movement, she spins mid-air sword dance, sword light forming circular energy wave spreading outward
6-7s: 24mm wide angle wide shot, warships torn apart and falling, flames and debris filling frame
7-8s: 85mm medium fixed shot, she hovers mid-air, clothes fluttering, looking back down at battlefield heroically, triumphant look catching breath
8-9s: handheld charging push, she thrusts sword into final flagship core
9-10s: 85mm close-up explosion, flagship completely disintegrates, flames engulf frame, victory freeze frame

Material details: silk hanfu fabric gloss and drape, metal sword energy glow effect, warship metal brushed texture and explosion sparks, volumetric cloud semi-transparent particle floating, ground debris burning texture

Camera: 24mm wide angle lens (battlefield panorama) + 85mm telephoto lens (close-up expression), handheld camera, fast motion, dynamic camera movement, wide angle to close-up rapid cuts, cinematic lighting, high contrast, dramatic lighting, light ratio 3:1

电影感画面，超写实质感，8K超高清，RAW原图，影视级调色

Speed tags: high-speed camera tracking, motion blur, speed lines, impact frames, dust and debris flying, energy sword trails, dynamic movement, fast-paced editing

Negative: no morphing, no extra limbs, no floating character disconnected from scene, no text watermark, no cartoon style, no 3D render, no neutral face, no static pose, no single continuous shot, no push-in only camera
```

---

## 打戏模块规则校验（7项自检）

- [x] 高速运动标签 ✅（`high-speed camera tracking`、`motion blur`、`speed lines`、`fast-paced editing`）
- [x] 表情变化描述 ✅（`fierce battle expression throughout`、`gritting teeth`、`intense focused eyes`、全片强制）
- [x] 至少3个切镜（10秒内10个镜头）✅
- [x] 角色融入场景 ✅（`tight lighting interaction`、`fully grounded in scene no floating feeling`）
- [x] 速度感/冲击感 ✅（`impact frames`、`dust and debris flying`、`explosion`）
- [x] 避免推镜头/一镜到底 ✅（`no single continuous shot`、10秒10镜）
- [x] 站位距离合理 ✅（`3-10 meters around character in combat distance`）

**7/7 全部通过** ✅

---

## 评分报告

| 维度 | 得分 |
|------|:---:|
| 完整性 | 30/30 |
| 准确性 | 40/40（色温5500K/5000K、焦段24mm/85mm、光比3:1） |
| 表现力 | 30/30 |
| 运动模式 | 10/10 |
| 打戏自检 | 7/7 |
| **总分** | **100/100** ✅ 满分 |

---

## 适用场景

| 标签 | 说明 |
|------|------|
| 东方科幻 | 未来空中战场 + 悬浮战舰 |
| 仙侠融合 | 唐制汉服女剑士 + 能量剑 |
| 高速打斗 | 穿梭/连斩/旋身剑舞 |
| 多镜头切换 | 10秒10镜，含24mm广角/85mm特写 |
| 大场面 | 战舰群爆炸/火焰/碎片/粒子特效 |
| 参考图控制 | 3张参考图锁定角色外观+表情 |
