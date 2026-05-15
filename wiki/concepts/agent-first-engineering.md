---
title: Agent-First Engineering
type: concept
status: active
created: 2026-05-10
updated: 2026-05-12
domain: agentic-software-engineering
tags:
  - wiki/concept
  - llm/agents
  - llm/coding
source_files:
  - raw/assets/工程技术：在智能体优先的世界中利用 Codex.md
  - raw/assets/Using Claude Code The Unreasonable Effectiveness of HTML使用 Claude 代码：HTML 的不可思议的有效性.md
---

# Agent-First Engineering

## 摘要

- Agent-first engineering 指一种软件工程工作方式: 团队默认把编码智能体当作主要实现者, 而把人类工程师的核心职责转向环境设计、任务分解、约束编码、验证机制和反馈回路。
- 在当前来源中, 这种模式的重点不是让智能体 "更努力", 而是让仓库、工具和文档结构变得更适合智能体稳定执行复杂任务。

## 关键要点

- 代码仓库应被设计成智能体可读的记录系统, 让架构、产品规范、执行计划和技术债都能在版本控制中被发现与验证。
- 大而全的单一说明书会挤占上下文并快速腐烂, 更有效的做法是使用简短地图式 `AGENTS.md` 加分层文档索引。
- 高吞吐量智能体工程依赖机械约束, 包括架构边界、结构测试、自定义 lint 和可自动修复的错误信息。
- QA 也要尽量转为智能体可执行, 例如让 UI、日志、指标、追踪和浏览器状态直接暴露给智能体。
- 除了让智能体更能执行, 也要让人类更能审阅: 面向人类的 HTML artifact 可以作为计划、评审与报告的高带宽回传界面, 帮助人在更复杂的 agent 流程中保持判断权。
- 完全自主会放大已有坏模式, 因此需要持续的垃圾回收式重构和把人类品味转写为规则。

## 证据与例子

- 文章把工程师的新角色概括为系统、架构和杠杆作用, 而不是手写实现。
- 作者明确提出 "给 Codex 一张地图, 而不是一本 1000 页的说明书", 用以说明上下文设计的重要性。
- 团队通过 doc-gardening 智能体、质量评分文档和后台重构任务持续维护仓库可读性。
- 另一篇来源进一步补充了面向人类的一侧: 当智能体输出越来越复杂时, 可以用 HTML artifact 而非长 Markdown 计划来提高可读性、分享性和交互性。

## 与 Dijkstra 窄界面的共鸣

- Dijkstra 在 EWD 667 中的窄界面论证与 agent-first 对结构化约束的强调高度一致: 刻意限制人机交互的语义带宽反而提高效率。
- 区别在于 agent-first 不排斥自然语言作为交互层, 但坚持在仓库与环境层面提供形式化约束和可自动验证的反馈。

## 张力或争议

- 这种模式目前依赖大量前期投资, 包括文档体系、lint、结构测试、浏览器与可观测性接入, 门槛不低。
- 文章主要基于单一团队经验, 尚不足以证明该方法在不同技术栈、合规环境或组织文化中都同样有效。
- 把审查和合并更多交给智能体会提升吞吐量, 但也可能引入新的盲区, 特别是在产品判断和长期架构演化上。

## 相关页面

- [Codex](../entities/codex.md)
- [Inference-Time Scaling](inference-time-scaling.md)
- [Natural Language Programming](natural-language-programming.md)
- [Edsger W. Dijkstra](../entities/edsger-dijkstra.md)
- [工程技术：在智能体优先的世界中利用 Codex](../sources/2026-harness-engineering-with-codex.md)
- [EWD 667: On the foolishness of "natural language programming"](../sources/dijkstra-natural-language-programming.md)
- [HTML Artifacts](html-artifacts.md)
- [使用 Claude Code：HTML 的不可思议的有效性](../sources/using-claude-code-html-effectiveness.md)

## 来源

- [工程技术：在智能体优先的世界中利用 Codex](../sources/2026-harness-engineering-with-codex.md)
