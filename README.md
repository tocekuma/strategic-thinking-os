# Strategic Thinking OS

> "拿着锤子看什么都是钉子。那就别只带一把锤子——带一整个工具箱。"

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude_Code-Skill-blue)](https://docs.anthropic.com)
[![Cursor](https://img.shields.io/badge/Cursor-Compatible-green)](https://cursor.sh)
[![AgentSkills](https://img.shields.io/badge/AgentSkills-Standard-purple)](https://github.com/tocekuma/strategic-thinking-os)

**五个脑子，一个调度台。**

把毛泽东、邓小平、安迪·格鲁夫、查理·芒格、以及互联网/AI 时代的方法论，
装进一个 skill，然后让一个"**元路由器**"根据你的问题自动选择最合适的分析框架。

不是给你五种语录让你自己选。是**系统帮你判断**该用哪个脑子、什么时候叠加多个脑子、什么时候一个框架就够。

---

## 为什么需要这个？

因为大部分人分析问题只有一个套路：

- 学了毛选的人，看什么都是"主要矛盾"
- 学了精益的人，看什么都是"MVP"
- 学了芒格的人，看什么都是"认知偏差"

**单一框架 = 单一盲区。**

这个 skill 的核心设计是：**你描述问题，它自动判断该用哪个框架，不该用哪个。**

---

## 五大思想体系

| 脑子 | 他最擅长回答的问题 | 什么时候叫他 |
|------|------------------|-------------|
| **毛泽东** | 我比对手弱，怎么赢？ | 竞争策略、市场进入、个人突围、以弱胜强 |
| **邓小平** | 我赢了/有了一摊子，怎么不翻车地改好？ | 组织改革、制度优化、从 1 到 N、转型 |
| **格鲁夫+德鲁克** | 我的团队/公司为啥不出活？行业要变天了怎么办？ | 管理效能、OKR、战略转折点、AI 转型 |
| **芒格** | 我是不是在犯蠢？ | 重大决策前的逆向检查、认知偏差扫描 |
| **现代方法论** | 互联网/AI 时代的打法有什么不同？ | OODA、精益、网络效应、平台策略、AI 竞争 |

---

## 元路由器怎么工作？

你丢一个问题进来，系统从**五个维度**判断：

```
1. 你是弱者还是强者？
   → 弱者 = 毛泽东    强者 = 格鲁夫+邓小平

2. 你的问题是竞争、治理、管理、还是决策？
   → 竞争 = 毛泽东    治理 = 邓小平    管理 = 格鲁夫    决策 = 芒格

3. 速度关键吗？
   → 关键 = 叠加现代框架（OODA/精益/Blitzscaling）

4. 关于人还是关于事？
   → 人 = 格鲁夫+统一战线    事 = 毛泽东+现代

5. 个人还是组织？
   → 个人 = 毛泽东(个人成长)+芒格    组织 = 组合判断
```

然后给你选出 **1-2 个主框架 + 辅助框架 + 芒格检验层（默认所有分析都跑一遍逆向检查）**。

---

## 实际效果长什么样？

### 案例：Anthropic 如何追赶 OpenAI？

五个脑子一起上：

| 脑子 | 他说的 |
|------|--------|
| **毛泽东** | 不打消费者市场（城市），在企业+开发者建根据地（农村） |
| **邓小平** | "Responsible Scaling" 不是道德行为，是改革路径——像经济特区 |
| **格鲁夫** | AI 是战略转折点。OpenAI 赌消费者入口，Anthropic 赌企业信任——两个不同的赌注 |
| **芒格** | 逆向：Anthropic 怎么保证输？→ 去跟 ChatGPT 抢消费者。所以别去 |
| **现代** | LLM API 没有网络效应 → 先发优势不牢 → 这对挑战者是好消息 |

**单用毛选只能看到"农村包围城市"。五体系一起上，还能看到"为什么不该 Blitzscale"、"安全不是情怀是战略"、"模型能力不是护城河"。**

完整案例见 `references/case-anthropic-openai.md`。

---

## 安装

### Cursor

```bash
git clone https://github.com/tocekuma/strategic-thinking-os.git ~/.cursor/skills/strategic-thinking-os
```

### Claude Code

```bash
git clone https://github.com/tocekuma/strategic-thinking-os.git ~/.claude/skills/strategic-thinking-os
```

装完在对话里说「战略分析」「帮我分析」「竞争策略」「管理问题」「逆向思维」「AI 竞争」之类的触发词就行。完整触发词列表在 SKILL.md 里。

---

## 文件结构

```
strategic-thinking-os/
├── SKILL.md                          元路由器 + 五体系速查（~200行）
├── README.md
├── LICENSE
└── references/
    ├── 00-meta-engine.md             多框架组合方法论 + 跨体系映射表
    ├── mao-core.md                   毛泽东六大框架精要
    ├── mao-cases.md                  商业 + 个人成长案例库
    ├── deng-reform.md                邓小平改革五大框架
    ├── deng-cases.md                 改革案例库（国家级 + 企业级）
    ├── grove-management.md           高产出管理 + OKR + 德鲁克精要
    ├── grove-inflection.md           战略转折点 + 穿越死亡谷
    ├── munger-models.md              心智模型 + 认知偏差清单 + 决策 checklist
    ├── modern-speed.md               OODA / 精益创业 / 闪电扩张
    ├── modern-platform.md            网络效应 / 平台策略 / 护城河理论
    ├── modern-ai-strategy.md         AI 时代竞争逻辑 / Scaling Laws / 开源 vs 闭源
    └── case-anthropic-openai.md      五体系联合分析完整示范
```

同样是渐进式加载——SKILL.md 当路由器，reference 按需读取，不浪费 token。

---

## 跟毛选 skill 的关系

| | [maoxuan-skill](https://github.com/tocekuma/maoxuan-skill) | strategic-thinking-os |
|-|-----|------|
| 思想体系 | 毛泽东（深度，12 框架 + 原文） | 毛泽东（精选 6 框架）+ 邓 + 格鲁夫 + 芒格 + 现代 |
| 适合 | 只想深入毛选 / 教员模式角色扮演 | 多视角交叉分析 / 复杂问题需要多个框架 |
| 独有特性 | 教员模式（第一人称）、原文论证链 | 元路由器、芒格检验层、AI 时代框架 |

简单说：**想请一个参谋 → maoxuan-skill。想开参谋会 → strategic-thinking-os。**

---

## 适用场景一览

- **竞争策略**："我们被大厂盯上了 / 要进一个新市场 / 如何差异化"
- **组织管理**："团队不出活 / OKR 怎么定 / 要不要重组"
- **改革转型**："传统业务怎么搞 AI / 公司要不要换方向"
- **重大决策**："A 和 B 方案选哪个 / 这个投资该不该做"
- **AI/互联网**："要不要做平台 / 网络效应在哪 / AI 护城河是什么"
- **个人成长**："30 岁转行 / 人生低谷 / 习惯养不成 / 不知道自己想做什么"

---

## License

[MIT](LICENSE) — 拿去用，不用写请示报告。

---

## 贡献

欢迎 Issue 和 PR。特别欢迎：
- 补充更多真实商业案例
- 增加新的思想体系模块（孙子兵法？克劳塞维茨？博弈论？）
- 翻译为英文/日文
- 修正框架描述中的事实错误
