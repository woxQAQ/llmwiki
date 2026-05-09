---
title: Inference-Time Scaling
type: concept
status: active
created: 2026-05-10
updated: 2026-05-10
domain: llm-inference
tags:
  - wiki/concept
  - llm/inference
source_files:
  - raw/assets/rlm.md
  - raw/assets/工程技术：在智能体优先的世界中利用 Codex.md
---

# Inference-Time Scaling

## 摘要

- Inference-time scaling 指通过增加推理阶段的计算、步骤或结构化流程, 提升模型回答质量的思路。
- 在这篇资料中, RLM 被视为继 CoT 式推理和 ReAct 式 agent 之后的一条新路径。

## 关键要点

- RLM 不是单纯增加 token 或思维链长度, 而是增加模型与上下文交互、递归分解和子调用的能力。
- 这种扩展路径理论上可通过强化学习等方式优化其搜索轨迹、效率和效果。
- 它把上下文管理本身变成推理阶段的可扩展计算。
- 新增的 Codex 工程案例提示, inference-time scaling 不只发生在单次回答里, 也可以体现在更长时间尺度的智能体运行、反馈循环和环境交互上。

## 证据与例子

- 文中明确将 RLM 描述为 general-purpose inference-time scaling 的潜在下一里程碑。
- 作者强调, 这种方式不要求单个模型调用必须原生处理极大上下文。
- `raw/assets/工程技术：在智能体优先的世界中利用 Codex.md` 则展示了另一种实践侧延展: 通过 PR 循环、可观测性查询、浏览器驱动和后台维护任务, 让编码智能体在较长运行中逐步完成复杂目标。

## 张力或争议

- 更强的 inference-time scaling 往往意味着更高延迟、更复杂调度与更难控成本。
- 不同任务上, 递归调用的收益是否能稳定超过检索、总结或外部工具链, 仍需更多证据。

## 相关页面

- [Recursive Language Models](recursive-language-models.md)
- [Long-Context Reasoning](long-context-reasoning.md)
- [Agent-First Engineering](agent-first-engineering.md)

## 来源

- [Recursive Language Models](../sources/2025-recursive-language-models.md)
- [工程技术：在智能体优先的世界中利用 Codex](../sources/2026-harness-engineering-with-codex.md)
