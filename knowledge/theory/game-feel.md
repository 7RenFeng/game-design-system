# 游戏手感（Game Feel）

> 手感是"手感好的游戏"与"能玩的游戏"的分水岭，也是平台跳跃类成败关键。
> 核心参考：Steve Swink《Game Feel》(2009) + 学术综述《Designing Game Feel》(2021)。

## 核心概念

手感 = 三个可拆解要素的组合：

```
手感 = 输入（Input） + 响应（Response） + 表现（Polish）
       玩家如何操作    角色如何反应    视听/物理反馈
```

1. **输入**：按键映射、输入延迟、缓冲（input buffer）、输入队列——"操作是否跟手"
2. **响应**：加速度、摩擦、重力、跳跃高度/时长（可变跳高！）、空中控制——"手感轻还是重"
3. **表现**：动画、粒子、屏幕震动、音效、顿帧（hit-stop）——"操作有没有重量感"

## 关键要点

1. **可变跳高**（variable jump）：按住跳得更高/更早松手跳得矮——现代平台跳跃手感标配（Celeste 也如此）。
2. **手感参数互相耦合**：改重力必须重调跳跃力与空中加速度；一次只调一个参数，实测对比。
3. **"飘" vs "重"**：手感方向由 加速度/最大速度/摩擦 三者比值决定——高加速度低摩擦=敏捷；低加速度高摩擦=厚重。
4. **表现层是"假物理"**：玩家感觉到的重量感很多来自视觉表现而非真实物理（顿帧、拉伸、尘土粒子）。
5. **调参流程（Celeste 验证）**：原型阶段每个参数一个开关/热键，实机改 → 立刻试 → 只保留"感觉对"的，别靠想象调。
6. **手感可测量**：输入→响应延迟 <100ms 基本"跟手"；跳跃前摇/落地后摇的可读性直接影响判定公平。

## 对本协作流程的用法

- **阶段 2 手感方向**：用词汇描述方向（轻盈敏捷/厚重扎实），不写死数值
- **阶段 4 数值表**：每个手感参数标注"↑/↓ 的体验影响"（TEMPLATE 已内置该列），方便原型期快速试
- **评审**："手感难调"是最大风险 → 缓解方案必须是"原型期调参流程"，不是"多写几版数值"
- **人机分工**：AI 给参数与调参工具，**人试玩拍板手感**——AI 判断不可靠（PROCESS.md 已规定）

## 来源

- [Steve Swink: Principles of Game Feel（书章节）](https://www.taylorfrancis.com/chapters/mono/10.1201/9781482267334-25/principles-game-feel-steve-swink)
- [Designing Game Feel: A Survey（2021 学术综述）](https://ar5iv.labs.arxiv.org/html/2011.09201)
- [Celeste Dev Explains How They Made Their Game Feel So Good](https://www.gamespot.com/articles/celeste-dev-explains-how-they-made-their-game-feel/1100-6474775/)
