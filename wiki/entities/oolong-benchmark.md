---
title: OOLONG Benchmark
type: entity
status: active
created: 2026-05-10
updated: 2026-05-10
domain: long-context-reasoning
tags:
  - wiki/entity
  - benchmark
source_files:
  - raw/assets/rlm.md
---

# OOLONG Benchmark

## 摘要

- OOLONG 是一个面向长上下文推理与细粒度信息聚合能力的 benchmark。
- 在 `raw/assets/rlm.md` 中, 它被用来验证 RLM 是否能缓解 context rot。

## 关键细节

- 文中重点讨论 `trec_coarse` 切分, 任务要求模型在数千条记录上做语义分类、过滤和计数。
- 该任务困难之处在于实例本身没有显式标签, 模型需要先理解再聚合。
- 作者强调, 即便输入长度仍在 GPT-5 或 GPT-5-mini 的上下文窗口内, 任务依然很难。

## 关系

- 与 [Recursive Language Models](../concepts/recursive-language-models.md) 紧密相关, 是其主要实验验证对象之一。
- 与 [Context Rot](../concepts/context-rot.md) 和 [Long-Context Reasoning](../concepts/long-context-reasoning.md) 直接相关。

## 相关页面

- [Recursive Language Models](../sources/2025-recursive-language-models.md)
- [Context Rot](../concepts/context-rot.md)

## 开放问题

- 目前 wiki 中关于 OOLONG 的信息仅来自这篇博客摘要, 还需要直接阅读 benchmark 原文。

## 来源

- [Recursive Language Models](../sources/2025-recursive-language-models.md)
