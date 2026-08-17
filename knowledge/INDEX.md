# 游戏设计知识库索引（Game Design Knowledge Base）

> 本库是 `game-design-system` 的知识层：方法论卡片 + 案例拆解 + 术语表。
> 用途：AI 在策划阶段推进时查对应卡片，作为提问依据、拟稿参考、评审 checklist 来源。
> 原则：**每张卡片 1 页精华**——核心概念 + 要点 + 对本协作流程的用法 + 来源。

## 使用场景 → 查什么

| 你在做什么 | 查 |
|---|---|
| 阶段 0 定义核心体验目标 | `theory/flow.md`（心流与体验）、`theory/core-loop.md` |
| 阶段 1 设计核心循环 | `theory/core-loop.md`、`cases/downwell.md`（单一机制）、`cases/spelunky.md` |
| 阶段 2 定三大支柱 | `theory/mda.md`（MDA 分层）、`theory/flow.md` |
| 阶段 3 功能清单/MVP | `theory/core-loop.md`（循环→功能映射） |
| 阶段 4 数值与手感 | `theory/game-feel.md`、`theory/balance.md` |
| 阶段 5 内容规划 | `theory/balance.md`（成长曲线）、`theory/randomness.md` |
| 阶段 6 风险 | `cases/celeste.md`（手感难调怎么破）、`theory/randomness.md`（随机性风险） |
| 评审验收"好不好玩" | `theory/game-feel.md`、`theory/flow.md` |
| 查术语 | `glossary.md` |

## 目录

### theory/ — 方法论卡片
| 文件 | 主题 | 一句话 |
|---|---|---|
| `mda.md` | MDA 框架 | 机制/动态/美学三层，设计者与玩家视角相反 |
| `core-loop.md` | 核心循环 | 分钟/小时/生涯三级循环 + 设计检验法 |
| `game-feel.md` | 游戏手感 | 手感 = 输入/响应/表现三要素，可测量可调优 |
| `flow.md` | 心流与难度曲线 | 挑战与能力匹配，心流通道、难度梯度设计 |
| `balance.md` | 数值平衡 | 成长曲线、标尺法、平衡验证方法 |
| `randomness.md` | 随机性与公平 | 随机≠不公平，可控随机与玩家代理权 |

### cases/ — 案例拆解
| 文件 | 案例 | 可借鉴 |
|---|---|---|
| `celeste.md` | Celeste | 手感打磨流程、模块化关卡、"死亡即教学" |
| `spelunky.md` | Spelunky | 程序生成的公平性、危险-回报信号设计 |
| `downwell.md` | Downwell | 单一机制的深度挖掘、手感即卖点 |

### templates/ — 题材变体模板
| 文件 | 题材 |
|---|---|
| `_placeholder.md` | （预留：RPG/肉鸽/模拟经营等变体，按需添加） |

## 来源说明

- 知识卡片基于公开资料（学术论文 / GDC 演讲 / 开发者访谈 / 行业文章）提炼，每张卡片末尾附来源链接
- 卡片是"提炼后的共识"，非原文搬运；引用时以来源为准
- 持续补充：新搜索、用户提供的教程/案例按同样格式入库

## 维护规则

1. 每张卡片：**概念 → 要点 → 协作用法 → 来源**，保持 1 页内
2. 新增卡片更新本索引表
3. 卡片内容过时/错误 → 修订并注明日期
4. 与 `TEMPLATE.md` / `PROCESS.md` 联动：模板章节引用的卡片路径写清楚
