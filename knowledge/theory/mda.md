# MDA 框架（Mechanics-Dynamics-Aesthetics）

> 游戏设计最经典的分析框架。来源：Hunicke, LeBlanc & Zubek, 2004《MDA: A Formal Approach to Game Design and Game Research》。

## 核心概念

游戏有三层，**设计者从机制往美学造，玩家从美学往机制感受**：

```
设计者视角（自下而上）          玩家视角（自上而下）
美学 Aesthetics ←←←←←←←←←←←←←← 玩家感受到的情绪/体验
  ↑                                 ↑
动态 Dynamics ←←←←←←←←←←←←←←←←  玩出来的系统行为
  ↑                                 ↑
机制 Mechanics ←←←←←←←←←←←←←←←←  规则、数据、算法
```

- **机制（Mechanics）**：规则与数据——能移动、能跳、速度 300、跳跃力 -480
- **动态（Dynamics）**：机制运行时的系统行为——"跳起时空中变向灵敏"、"连招节奏"
- **美学（Aesthetics）**：玩家体验到的情绪——8 类：感官快感 / 幻想 / 叙事 / 挑战 / 同伴 / 发现 / 表达 / 消遣

## 关键要点

1. **视角反转**：设计失败常因"从机制出发想美学"。应先定美学（玩家该有什么感觉），再设计机制实现它。
2. **8 类美学清单**（desired aesthetics）：定核心体验目标时从这 8 类里挑，避免空泛的"好玩"。
3. **消费层（consumption layer）**：同一套机制 + 不同动态规则 = 不同体验（如道具赛 vs 计时赛）。

## 对本协作流程的用法

- **阶段 0**：核心体验目标 = 从 8 类美学里选 1~3 个（如"挑战+发现"）
- **阶段 2**：三大支柱先回答"玩家要什么美学体验"，再定机制
- **评审**：检查"机制改动是否服务目标美学"——机制砍不掉时，问它服务哪个美学
- **沟通**：人用美学词汇描述感受（"手感飘"），AI 转成机制参数（重力/加速度），这是人机协作的共同语言

## 来源

- [MDA: A Formal Approach to Game Design and Game Research（原文 PDF）](https://core.ac.uk/download/301299077.pdf)
- [Mechanics, Dynamics, and Aesthetics - 教学版解读](https://pressbooks.usnh.edu/creatinggames/chapter/mechanics-dynamics-and-aesthetics/)
