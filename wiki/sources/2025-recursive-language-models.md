---
title: Recursive Language Models
type: source
status: active
created: 2026-05-10
updated: 2026-05-10
domain: long-context-reasoning
tags:
  - wiki/source
  - llm/long-context
  - llm/inference
source_files:
  - raw/assets/rlm.md
---

# Recursive Language Models

## 摘要

- 这篇博客提出 Recursive Language Models, RLM 作为一种推理时 inference scaffold, 让语言模型在给出最终答案前递归调用自身或其他模型。
- 核心思想不是把超长上下文直接塞进一次模型调用, 而是把上下文放进一个环境里, 让根模型按需查看、切分、筛选、总结并发起子查询。
- 文中重点论证 RLM 可以缓解 context rot, 扩展有效上下文长度, 并提供一种新的 test-time inference scaling 路径。
- 作者给出的具体实现是 Python REPL notebook 风格环境, 其中上下文被预加载为变量, 根模型通过代码块与环境交互。

## 关键信息

- RLM 对用户暴露的接口仍像普通模型调用, 但内部允许递归 LM 调用与环境交互。
- 文章强调这是 context-centric decomposition, 即按上下文结构而非按任务步骤做拆解。
- 在 OOLONG 长上下文基准上, 文中报告 `RLM(GPT-5-mini)` 在困难切分上显著优于直接使用 `GPT-5` 或 `GPT-5-mini`。
- 在 BrowseComp-Plus 风格的大语料检索与多跳问答任务上, 文中报告 RLM 在 100 到 1000 文档规模下保持更稳定表现。
- 作者认为 RLM 不是传统 agent 的简单变体, 而是让模型自己决定如何分解上下文。

## 相关实体

- [OOLONG Benchmark](../entities/oolong-benchmark.md)
- [BrowseComp-Plus](../entities/browsecomp-plus.md)

## 相关概念

- [Recursive Language Models](../concepts/recursive-language-models.md)
- [Context Rot](../concepts/context-rot.md)
- [Inference-Time Scaling](../concepts/inference-time-scaling.md)
- [Long-Context Reasoning](../concepts/long-context-reasoning.md)

## 值得记录的证据

- 文中把 RLM 定义为在环境 `E` 中运行的更具表现力的 LM 调用, 允许对上下文进行查看、切分、变换和递归子查询。
- 作者报告 `RLM(GPT-5-mini)` 在 OOLONG 的困难长上下文设置上比 `GPT-5` 多出超过 34 分, 并且平均成本接近或更低。
- 在 BrowseComp-Plus 子集实验中, 作者报告 `RLM(GPT-5)` 在 1000 文档规模下保持高表现, 相比直接模型调用和 BM25/agent 基线更稳。
- 文中明确指出当前实现仍有速度与异步不足的问题, API 成本与运行时间也缺乏强控制。

## 开放问题

- 这些结果主要来自博客中的早期实验, 需要结合论文与代码仓库进一步核实方法细节。
- RLM 与现有 agent、retrieval、summarization scaffold 的边界在真实产品中如何划分, 仍需更多案例。
- 当基础模型上下文能力继续增长时, RLM 的相对收益会如何变化, 还有待验证。

## 来源

- 原始文件: `raw/assets/rlm.md`
- 博客中提到的论文: `https://arxiv.org/abs/2512.24601v1`
- 代码仓库: `https://github.com/alexzhang13/rlm`
