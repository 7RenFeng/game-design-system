# 心流与难度曲线（Flow & Difficulty Curve）

> 玩家沉浸（心流）理论：挑战与能力匹配时进入心流通道。
> 来源：Csikszentmihalyi 心流理论 + 游戏行业实践（Flow in Games, GDC）。

## 核心概念

玩家能力 vs 游戏挑战 的关系决定体验：

```
挑战难度
  ↑
 高 |  焦虑区(挑战>能力)    ← 太难得不到正反馈
 中 |      ★ 心流通道 ★     ← 挑战≈能力，沉浸
 低 |  无聊区(挑战<能力)    ← 太简单无意义
     +---------------------→ 玩家能力（随时间增长）
```

- **心流通道**：挑战略高于能力（8% 左右），失败可重试、反馈即时
- 玩家的能力**随游戏时长增长** → 挑战必须**同步上升**，否则滑入无聊区
- 难度曲线 = 设计者安排的挑战随时间的变化线

## 关键要点

1. **难度曲线设计**（Development of Difficulty）：难度阶梯式上升 + 周期性回落（每关结尾喘息点），不是直线。
2. **阶梯结构**：新机制先安全教学 → 组合使用 → 压力测试（Celeste 的"一个机制一章"就是这种结构）。
3. **心流破坏者**：卡关（无路径提示）、惩罚过重（死了重来 10 分钟）、反馈延迟、目标模糊。
4. **焦虑区也有价值**：boss 战/极限挑战故意进焦虑区，但**必须给学习路径**（死亡即教学：死了立刻知道为什么）。
5. **衡量方法**：试玩观察"挫败皱眉 vs 面无表情 vs 无聊走神"，三态分布 ≈ 难度曲线的体检报告。
6. **动态难度**（可选）：隐形调整（橡皮筋机制）要谨慎，玩家反感"被操纵"。

## 对本协作流程的用法

- **阶段 0 目标时长**：目标时长决定难度曲线跨度（3 分钟单局 vs 5 小时通关，曲线完全不同）
- **阶段 5 内容规划**：关卡数 = 难度曲线的节点数，每关标"引入/巩固/压力"角色
- **评审**："内容量级合理"检查项 → 数一下难度曲线有没有断层（第 N 关难度跳变过大？）
- **案例参照**：`cases/celeste.md`（阶梯教学典范）、`cases/spelunky.md`（随机环境下的难度把控）

## 来源

- [Welcome to Flow in Games](http://www.jenovachen.com/flowingames/foundation.htm)
- [Development of Difficulty in Games](https://www.gamedeveloper.com/design/development-of-difficulty-in-games)
- [Hierarchy of challenges – Game Design & Development 教材](https://ecampusontario.pressbooks.pub/gamedesigndevelopmenttextbook/chapter/hierarchy-of-challenges/)
