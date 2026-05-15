---
title: Natural Language Programming
type: concept
status: active
created: 2026-05-10
updated: 2026-05-15
domain: programming-languages
tags:
  - wiki/concept
  - programming-languages
  - natural-language
  - formal-methods
  - llm
source_files:
  - raw/assets/e-w-dijkstra-on-the-foolishness-of-natural-language-programming-ewd-667.md
---

# Natural Language Programming

## 摘要

- Natural language programming (NLP, 自然语言编程) 是指用人类自然语言 (英语、中文等) 而非形式编程语言来指示计算机执行任务的构想。
- Dijkstra 在 1970 年代末以 EWD 667 对其进行了激烈批判, 认为形式符号系统是必要而非负担。LLM 时代的 prompt 编程在某种意义上实现了这一构想, 但也带来了新的精确性、可验证性和界面设计问题。

## 关键论点 (来自 Dijkstra)

### 形式系统的必要性

- 形式符号系统的核心价值不在于 "为难人", 而在于用极少数简单规则就能排除大量无意义的表达。自然语言的 "自然性" 恰恰在于它的模糊容忍度——可以轻松说出 "nonsense 不明显的话"。
- 数学与计算的历史表明, 从口头/修辞文体到形式符号系统的跃迁是文明级别的进步。

### 窄界面论证

- 人与机器之间的界面不是固定工作量的分配, 跨界面沟通本身会新增成本。自然语言界面看似把负担推向机器, 实际上两端都可能变得更困难。
- "窄界面"——刻意限制交互的语义带宽——反而更高效。

### 自然语言编程的 "黑魔法 bootstrap" 问题

- 如果从一开始就只有自然语言作为人机界面, 计算机科学的全部智力可能都要消耗在从自然语言引导出可用形式系统的过程中, 而这一过程可能极其漫长。

## LLM 时代的新张力

### Prompt 编程算不算自然语言编程?

- 现代 LLM 允许用户用自然语言描述需求并生成代码、执行任务。这在某种意义上实现了自然语言编程的愿景。
- 但 prompt engineering 的实践正在迅速发现: 结构化 prompt、约束格式、少样本示例、类型系统式描述等方式才能获得可靠结果——这恰恰向着形式化方向回归。

### Agent-first engineering 的回应

- Agent-first engineering 主张给 agent "地图而非千页说明书", 强调结构化接口、机械约束和可验证规则。这在精神上高度接近 Dijkstra 的窄界面论证。
- 区别在于: agent-first 并不排斥自然语言作为交互层, 但坚持在仓库设计层面提供形式化的约束与反馈回路。

### 精确性与模糊性的权衡

- 自然语言 prompt 的低门槛使非程序员也能参与软件创建, 这是 Dijkstra 未曾讨论的民主化视角。
- 但低门槛也意味着更容易产生 "仔细阅读后毫无意义的废话"——prompt 的 nonsense 可能被 LLM 热情执行, 产生难以察觉的错误输出。

## 开放问题

- 自然语言 prompt + 形式化验证 (如测试、类型检查、lint) 的组合是 Dijkstra 会认可的折中吗?
- "窄界面" 在 LLM agent 工具设计中如何操作化? 工具描述应该有多自然、多形式?
- 自然语言编程的 "新文盲" 风险是否在 LLM 生成的文本中加速扩散?

## 相关页面

- [EWD 667: On the foolishness of "natural language programming"](../sources/dijkstra-natural-language-programming.md)
- [Edsger W. Dijkstra](../entities/edsger-dijkstra.md)
- [Agent-First Engineering](agent-first-engineering.md)
- [Context Rot](context-rot.md)
