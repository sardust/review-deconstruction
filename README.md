# review-deconstruction

## 这是什么？/ What is this?

这是一个 **[WorkBuddy](https://www.workbuddy.cn) Skill**（技能包），名字叫**「综述拆解法」**。

科研新手写文献综述时最大的困境是：读了很多综述，却依然不知道怎么写综述——因为**读普通论文是"读内容"，读综述是"读写法"**，这是两种完全不同的阅读方式。这个 Skill 把"拆解综述写作工艺"的方法论固化下来，让 AI 助手在你写综述之前，先陪你把领域里的标杆综述逐篇拆开：它的章节主线怎么选、分类树怎么画、段落怎么串联、对比表怎么设计、挑战清单怎么组织——然后给你一份**「抄 3 样、避 2 样」**的写作决策清单。

**它解决什么问题**：把你从"读完 50 篇综述还是不会写"里救出来，变成"拆 3 篇就知道自己的综述该怎么搭"。

**适合谁**：正在（或即将）写文献综述的研究生、博士生、科研人员；也适合任何想系统学习学术写作的人。

**它是怎么工作的**（30 秒版）：对每篇目标综述执行「三遍阅读 → 8 问拆解 → 抄 3 避 2 判决 → 副产品记录」；拆解 ≥2 篇后，再聚合成交叉对比的**写作决策清单**（哪些写法是共识该采纳、哪些是通病该规避、哪些存在分歧需你主动选择）。

**典型使用场景**：
- 你说："拆解这篇综述 PDF" → AI 输出一份填写完整的拆解表（含原句证据）
- 你说："我在写文献综述，先研究三篇标杆综述的写法" → 产出三份拆解表 + 一份写作决策清单
- 你说："这篇综述值不值得当我的范本？" → 给出明确的抄/避判决

## 核心理念 / Core Principle

> 读普通论文是"读内容"，读综述是"读写法"。
> Read ordinary papers for content; read reviews for craft.

每篇拆解必须落到具体决策：**抄 3 样、避 2 样**。
Every deconstruction ends with concrete decisions: copy 3 things, avoid 2 things.

## 内容 / Contents

```
review-deconstruction/
├── SKILL.md                              # 主流程：三遍阅读 → 8 问拆解 → 抄3避2 → 多篇聚合
├── assets/
│   └── deconstruction-template.md        # 空白拆解表模板（每篇综述复制一份填写）
└── references/
    ├── worked-example-thaker-2025.md     # 完整填写示范（中等质量综述，兼示可抄与可避）
    └── multi-review-synthesis.md         # 多篇拆解的聚合方法（写作决策清单）
```

## 安装 / Install

下载 `dist/review-deconstruction.zip`，在 WorkBuddy 中通过技能管理导入即可。

Download `dist/review-deconstruction.zip` and import it via WorkBuddy's skill management.

## 触发示例 / Trigger Examples

- "拆解这篇综述 PDF"
- "帮我看看这篇 review 是怎么写的"
- "我在写文献综述，先研究三篇标杆综述的写法"
- "对比这几篇综述，给我一份写作决策清单"

## License

MIT
