# 随机性与公平（Randomness & Fairness）

> 随机性让内容"用不完"，但玩家要的是"可控的随机"——危险可以预见，选择有代理权。
> 核心参考：Spelunky 设计分析系列（Rami Ismail / Derek Yu 社区分析）。

## 核心概念

随机 ≠ 不公平。区别在**信息是否可读、失败是否可归因**：

```
随机性（如程序生成关卡）
   ↓ 设计关键
信息透明度：玩家能否预见危险？
失败归因：死了，是"我失误"还是"系统耍我"？
玩家代理权：随机之后，玩家是否有选择余地？
```

## 关键要点

1. **可控随机**（Spelunky 范式）：
   - 生成器有**约束规则**（保证通路存在、关键道具可达），不是纯随机撒
   - **危险-回报信号**：高风险区域视觉可辨（尖刺/深渊一眼可见），玩家自己决定赌不赌
2. **确定性内核 + 随机表皮**：核心挑战公平（所有玩家同一规则），随机只变内容排列
3. **"它是对的狠"**（It's all right to be mean）：Spelunky 允许"恶意"设计，但**必须公平**——玩家死了能说出"我为什么死"
4. **随机性风险**：
   - 生成出死局（无解关卡）→ 必须有规则兜底
   - 玩家遇到极端序列（连续好运/厄运）→ 用加权/洗牌而非独立随机
   - 学习曲线被随机打乱 → 前期随机度低，后期放开
5. **测试方法**：随机生成器要跑海量模拟（生成 1 万关看无解率），不能只靠试玩。

## 对本协作流程的用法

- **阶段 5 内容规划**：若含随机生成，内容量级 = "生成器规则数"而非"手工关卡数"
- **阶段 6 风险**："随机性失控"是高危风险 → 缓解：约束规则 + 模拟测试 + 风险视觉化
- **评审**："循环完整"检查项 → 随机内容是否仍保证核心循环可达
- **案例参照**：`cases/spelunky.md`

## 来源

- [A Spelunky Game Design Analysis - Pt. 2](https://www.gamedeveloper.com/design/a-spelunky-game-design-analysis---pt-2)
- [Fairness, Discovery & Spelunky](https://www.gamedeveloper.com/design/fairness-discovery-spelunky)
- [Spelunky: It's all right to be mean](https://www.gamedeveloper.com/business/-i-spelunky-i-it-s-all-right-to-be-mean)
