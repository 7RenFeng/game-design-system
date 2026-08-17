# 数值平衡（Game Balance）

> 数值是玩法的"物理"，平衡是让每个选择都值得、每个阶段都有成长感。
> 核心参考：Ian Schreiber & Brenda Romero《Game Balance》(2021) + 独立开发实践。

## 核心概念

平衡 = 让系统的**选择有意义** + **成长有感知** + **难度有梯度**。

三个层面：
1. **成长曲线**（progression）：玩家的能力/数值随时间增长——曲线形状决定"升级爽感"
2. **难度曲线**（difficulty）：敌人/关卡强度随时间增长——必须与成长曲线匹配（见 `flow.md`）
3. **选择平衡**（trade-offs）：玩家可选方案各有优劣，没有"唯一最优解"

## 关键要点

1. **标尺法**（gameres 经典）：先定"标尺单位"（如 1 秒 = 1 伤害），所有数值用标尺推导，可对齐可审查。
2. **成长曲线形状**：
   - 线性：平稳，适合休闲
   - 指数：前期快后期爆炸，适合刷宝
   - S 形/分段：平台期+突破期交替，最有"阶段感"（每章一次突破）
3. **平衡验证方法**：
   - 数学推演（DPS 计算表）
   - 模拟测试（脚本跑 1 万次战斗看胜率分布）
   - 实机试玩（人最可靠）
   - 数据埋点（上线后看各数值使用率/胜率偏离）
4. **经济平衡**（若含资源系统）：产出 vs 消耗的闭环；通货膨胀（数值失控）是最大杀手。
5. **调参纪律**：一次只改一个参数 → 记录 → 对比；用表格管理参数（TEMPLATE 数值表即此用途）。

## 对本协作流程的用法

- **阶段 4 数值表**：初始值 + "↑/↓ 影响"列 + 调优目标（TEMPLATE 已内置）；用标尺法让 AI 拟稿有据
- **评审**："数值有初始值"检查项 → 每个玩法参数都有初始值可测
- **案例参照**：成长曲线形状决策写 ADR（改曲线=改核心体验）

## 来源

- [Ian Schreiber & Brenda Romero: Game Balance（书）](https://www.taylorfrancis.com/chapters/mono/10.1201/9781315156422-29/absolute-references-ian-schreiber-brenda-romero)
- [Game Economy Balancing With Spreadsheets: A Practical Guide for Indie Developers](https://www.strayspark.studio/blog/game-economy-balancing-spreadsheets)
- [游戏成长周期设计基础：用"标尺"去衡量（中文）](https://www.gameres.com/461152.html)
