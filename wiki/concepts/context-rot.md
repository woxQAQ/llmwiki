---
title: Context Rot
type: concept
status: active
created: 2026-05-10
updated: 2026-05-10
domain: long-context-reasoning
tags:
  - wiki/concept
  - llm/long-context
source_files:
  - raw/assets/rlm.md
---

# Context Rot

## 摘要

- Context rot 指随着上下文变长, 模型对上下文中信息的调用、聚合与推理能力下降的现象。
- 它不只是“能不能找到 needle”问题, 更像是长会话或超长提示下整体推理质量逐渐退化。

## 关键要点

- 一些简单长上下文 benchmark 可能低估了这个问题, 因为模型即使在大上下文中也能做局部检索。
- 真正困难的场景是需要在大量细粒度信息上做聚合、计数、多跳关联或长期对话保持一致性。
- RLM 的主要动机之一就是避免让单次模型调用直接承受整段巨大上下文。

## 证据与例子

- `raw/assets/rlm.md` 中将 context rot 作为 RLM 设计的核心背景, 并指出 bloated chat history 与长代码会话是典型体验场景。
- OOLONG 结果被用来说明, 即使输入理论上放得进上下文窗口, 性能仍可能因上下文过长而退化。

## 张力或争议

- Context rot 的准确定义与可测量方式仍不稳定。
- 退化来源可能混合了训练分布偏移、注意力负担、任务复杂度和系统实现等因素。

## 相关页面

- [Recursive Language Models](recursive-language-models.md)
- [Long-Context Reasoning](long-context-reasoning.md)

## 来源

- [Recursive Language Models](../sources/2025-recursive-language-models.md)
