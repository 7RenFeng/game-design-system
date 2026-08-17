# 案例拆解：Spelunky（洞穴探险）

> 程序生成关卡 + 公平性设计的教科书。可借鉴：可控随机、危险-回报信号、循环设计。

## 项目速览

- 类型：Roguelike 平台跳跃
- 规模：程序生成关卡，每次开局全新地图，一命通关
- 卖点：**每次冒险都不同** + 公平的"恶意"
- 核心体验目标：发现 + 挑战 + 表达（玩家风格化冒险）

## 设计拆解

### 1. 程序生成的"公平性"（Fairness）
- **约束生成**：生成器保证每个区域通路可达、关键道具（如钥匙/绳索）必然出现——不是纯随机
- **危险可读**：陷阱/敌人/深渊视觉信号清晰，玩家能预见风险
- **失败可归因**：玩家死时永远能说清"我为什么死"——是判断失误，不是系统耍人
- **代理权**：随机地形给出选择（绕路 vs 冒险拿宝），玩家有决策空间

### 2. 危险-回报设计（Risk-Reward）
- 高风险高回报：深坑往往藏着宝，但掉下去可能死
- **"It's all right to be mean"**：允许恶意设计（炸弹炸出的隐藏层），但恶意必须符合物理规则、可预测

### 3. 循环设计（Core Loop）
- 分钟级：探索 → 拿宝 → 避险 → 进入下一层
- 小时级：每次开局随机 → 学新道具组合 → 挑战更深层
- 生涯级：速通/挑战模式/隐藏结局 → 技巧成长，运气只是变量

### 4. 系统涌现（Emergence）
- 少量规则（物品×地形×怪物交互）产生大量玩法组合——"用系统复杂度代替内容量"

## 可借鉴到本协作流程

| Spelunky 做法 | 对应到我们的流程 |
|---|---|
| 约束生成 + 模拟测试 | 阶段 6 风险："随机失控"缓解 = 生成器约束规则 + 跑 1 万次模拟 |
| 危险-回报信号 | 关卡/敌人设计标注"风险可读性" |
| 系统涌现 | 内容规划时优先"规则组合"而非"堆内容" |
| 循环三尺度 | 阶段 1 直接抄这个三级循环结构 |

## 来源

- [A Spelunky Game Design Analysis - Pt. 2](https://www.gamedeveloper.com/design/a-spelunky-game-design-analysis---pt-2)
- [Fairness, Discovery & Spelunky](https://www.gamedeveloper.com/design/fairness-discovery-spelunky)
- [Spelunky: It's all right to be mean](https://www.gamedeveloper.com/business/-i-spelunky-i-it-s-all-right-to-be-mean)
- [How Spelunky got its procedural 'hook' & actually got finished](https://www.gamedeveloper.com/design/how-i-spelunky-i-got-its-procedural-hook-actually-got-finished)
