---
title: BrowseComp-Plus
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

# BrowseComp-Plus

## 摘要

- BrowseComp-Plus 是一个把潜在相关文档预下载好的 deep research benchmark, 用于评估跨大量文档的多跳检索与问答。
- 在 `raw/assets/rlm.md` 中, 它被用来测试 RLM 在 10 到 1000 文档甚至更大规模语料上的表现。

## 关键细节

- 查询往往需要跨多个文档建立关联, 不是找到单个答案文档就能结束。
- 文中将其视为评估“大规模上下文下的信息查找与组合”的理想测试场景。
- 作者报告 RLM 在文档数提升时比直接模型调用和若干 BM25 基线更稳定。

## 关系

- 与 [Recursive Language Models](../concepts/recursive-language-models.md) 相关, 是验证其超大上下文处理能力的实验对象之一。
- 与 [Long-Context Reasoning](../concepts/long-context-reasoning.md) 和 [Inference-Time Scaling](../concepts/inference-time-scaling.md) 相关。

## 相关页面

- [Recursive Language Models](../sources/2025-recursive-language-models.md)
- [Long-Context Reasoning](../concepts/long-context-reasoning.md)

## 开放问题

- 文中实验只覆盖该 benchmark 的一个小子集, 需要后续资料补充完整评估情况。

## 来源

- [Recursive Language Models](../sources/2025-recursive-language-models.md)
