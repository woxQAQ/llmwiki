---
title: Recursive Language Models
type: concept
status: active
created: 2026-05-10
updated: 2026-05-10
domain: long-context-reasoning
tags:
  - wiki/concept
  - llm/architecture
  - llm/inference
source_files:
  - raw/assets/rlm.md
---

# Recursive Language Models

## 摘要

- Recursive Language Models, RLM, 是一种推理时框架, 让模型在回答问题前通过环境与递归子调用来处理长上下文。
- 它保持“像一次模型调用”的接口, 但把上下文管理从固定外部流程转移给模型自己决定。

## 关键要点

- RLM 的核心不是更大的单次上下文窗口, 而是更灵活的上下文访问方式。
- 根模型只直接接收 query, 上下文放在环境中按需访问。
- 递归子调用可用于 peeking、grepping、partition plus map、summarization 等策略。
- 这种方法把“如何拆解上下文”本身变成可学习、可优化的推理过程。

## 证据与例子

- 文中给出的主要实现是 Python REPL 环境, 其中上下文以变量形式存在, 模型通过代码查看片段、筛选内容、调用子模型并拼装最终答案。
- 在 OOLONG 和 BrowseComp-Plus 的实验里, 作者报告 RLM 在长上下文和超大文档集合任务上优于若干直接调用与检索基线。

## 张力或争议

- 当前证据主要来自早期博客与初版论文, 外部复现仍然重要。
- RLM 是否优于更成熟的 agent scaffold, 很大程度取决于任务类型、延迟预算和工程实现。
- 递归调用提升效果的同时也引入成本、调度和可控性问题。

## 相关页面

- [Context Rot](context-rot.md)
- [Inference-Time Scaling](inference-time-scaling.md)
- [Long-Context Reasoning](long-context-reasoning.md)
- [Recursive Language Models](../sources/2025-recursive-language-models.md)

## 来源

- [Recursive Language Models](../sources/2025-recursive-language-models.md)
