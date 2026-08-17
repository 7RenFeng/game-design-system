# 核心循环（Core Loop）设计

> 核心循环是玩家反复做的最小动作闭环，是整个游戏设计的锚。设计文档里"核心循环未定不前进"。

## 核心概念

玩家在游戏里**反复执行**的动作序列，每个循环给出反馈，激励下一次循环：

```
动作 → 反馈 → 成长/变化 → 更复杂的动作 → …
```

专业做法拆**三个时间尺度**（TEMPLATE.md 已内置此结构）：

| 尺度 | 问题 | 示例（平台跳跃） |
|---|---|---|
| 分钟级 | 玩家每一分钟做什么？ | 移动 → 跳跃过台 → 到终点 → 下一关 |
| 小时级 | 为什么玩一小时/一天？ | 通关新关 → 解锁新机制 → 挑战更难 |
| 生涯级 | 为什么玩一周/一月？ | 全 S 评分 → 速通 → 成就/排行 |

## 关键要点

1. **循环必须闭环**：动作后必须有反馈和回报，否则是"单向任务"不是循环。
2. **压缩循环（compulsion loop）**：社交/放置游戏常用"短循环高回报"（如 5 分钟一收菜），GDC 有专门方法（Turducken 法：循环套循环）。
3. **单一机制挖深（Downwell 范式）**：一个机制做到极致可支撑整个游戏，比 10 个浅机制强。
4. **设计检验三问**（Gamedeveloper 的 3 Questions）：
   - 玩家在做什么？（明确动作）
   - 为什么有趣？（情绪/挑战/奖励）
   - 什么时候无聊？（循环断点 → 该加变化了）
5. **循环→功能映射**：功能清单里的每项 P0 都应能在循环图里找到位置；循环里没有的功能不配进 MVP。

## 对本协作流程的用法

- **阶段 1**：产出三级循环图（文字版），未闭环禁止进阶段 2
- **阶段 3**：用循环图反推功能清单——循环的每个环节 = 至少一个功能
- **评审**：问"循环哪个环节会让人 10 分钟就腻？" → 缺变化/缺难度上升
- **案例参照**：`cases/downwell.md`（单一机制）、`cases/spelunky.md`（循环+随机变化）

## 来源

- [Video: Building killer game loops in social games](https://www.gamedeveloper.com/business/video-building-killer-game-loops-in-social-games)
- [GDC Vault: The "Turducken" Method — Compulsion Loops](https://gdcvault.com/play/1014958/)
- [3 Questions That Will Help You Make a More Engaging Experience](https://www.gamedeveloper.com/design/3-questions-that-will-help-you-make-a-more-engaging-experience)
