---
title: RLM、ReAct 与 RAG 的对比
type: analysis
status: active
created: 2026-05-10
updated: 2026-05-10
domain: long-context-reasoning
tags:
  - wiki/analysis
  - llm/long-context
  - llm/inference
source_files:
  - raw/assets/rlm.md
---

# RLM、ReAct 与 RAG 的对比

## 问题

- 在长上下文与大规模资料处理场景下，Recursive Language Models、ReAct 类 agent 与传统 RAG 各自更适合解决什么问题？

## 结论

- 如果任务的核心难点是“如何在超长上下文里动态查看、切分、聚合并推理”，RLM 更有吸引力。
- 如果任务已经有明确工具链，且需要多步外部行动，例如搜索、浏览、执行工具，ReAct 更自然。
- 如果任务主要是“从大语料里找相关片段并回答”，而且证据定位比复杂聚合更重要，RAG 往往是更便宜、更成熟的默认方案。
- 从 `raw/assets/rlm.md` 的论证看，RLM 的优势主要体现在 context rot、超长输入与复杂聚合任务上，而不是取代所有检索或 agent 系统。

## 对比表

| 维度                | RLM                | ReAct                                  | RAG                |
| ----------------- | ------------------ | -------------------------------------- | ------------------ |
| 核心思路              | 让模型在环境中递归处理上下文     | 让模型按 thought-action-observation 循环调用工具 | 先检索相关片段，再基于片段回答    |
| 主要分解方式            | 按上下文结构分解           | 按任务步骤分解                                | 按相关性筛选证据           |
| 更适合的问题            | 长上下文聚合、多跳推理、长输入长输出 | 搜索、浏览、调用工具、执行外部动作                      | 知识问答、证据定位、标准检索增强回答 |
| 对 context rot 的应对 | 强，避免根模型直接吞下全部上下文   | 中，取决于 agent 轨迹与工具设计                    | 弱到中，依赖检索是否能准确召回    |
| 工程复杂度             | 高，需要环境、递归调度、成本控制   | 中到高，需要工具编排与状态管理                        | 中，检索与重排体系相对成熟      |
| 可解释性              | 中到高，可查看上下文访问与子调用轨迹 | 高，可查看动作轨迹                              | 中，能看召回片段，但聚合逻辑较弱   |
| 成本与延迟             | 可能较高，尤其在递归较深时      | 常偏高，取决于动作轮数                            | 通常较低，尤其在检索系统成熟时    |

## 关键区别

### 1. 分解对象不同

- RLM 的出发点是上下文太大、太乱或太难直接整体理解，因此让模型自己决定如何 peek、grep、chunk、summarize、recurse。
- ReAct 的出发点是任务需要一连串动作，因此让模型决定何时搜索、何时调用工具、何时继续推理。
- RAG 的出发点是没必要把所有材料都交给模型，先通过检索缩小证据范围，再做回答。

### 2. 对长上下文问题的态度不同

- RAG 默认认为“先找相关片段”通常足够，因此很依赖检索质量。
- ReAct 默认认为“遇到问题就多走几步工具调用”可以逐步逼近答案。
- RLM 则认为在某些任务里，问题不只是找片段，而是需要对上下文本身进行程序化、递归式的操作。

### 3. 对复杂聚合任务的支持不同

- `raw/assets/rlm.md` 里的 OOLONG 例子强调，难点在于要对数千条记录做语义分类、过滤与计数，这不只是检索一两段证据能解决的事。
- 在这类任务上，RLM 可以先筛、再分块、再对子块发起子查询，因此比直接模型调用或简单检索更有优势。
- 如果任务只需要找到一两个强相关片段，RAG 往往没有必要被更复杂的 RLM 替代。

## 从当前资料得出的判断

- 对 [OOLONG Benchmark](../entities/oolong-benchmark.md) 这类细粒度聚合问题，RLM 的相对优势最明显。
- 对 [BrowseComp-Plus](../entities/browsecomp-plus.md) 这类超大文档集合上的多跳问题，RLM 也显示出比若干 BM25 与 ReAct 基线更稳定的趋势。
- 但当前证据主要来自一篇早期博客与作者自己的实验汇报，因此更适合作为“值得认真跟踪的方向”，而不是已经彻底定论的范式胜利。

## 缺口与不确定性

- 当前 wiki 只有一篇 RLM 来源资料，缺少对 ReAct、RAG、本地检索或 memory 系统的独立来源页支撑。
- 这里对 RAG 与 ReAct 的比较，部分来自通用方法理解，部分来自 `raw/assets/rlm.md` 中对基线的描述，后续最好补更多原始文献。
- 不同系统的效果高度依赖具体实现；“RLM 优于 RAG”或“RLM 优于 ReAct”不能脱离任务分布、延迟预算和工程质量单独成立。

## 相关页面

- [Recursive Language Models](../concepts/recursive-language-models.md)
- [Context Rot](../concepts/context-rot.md)
- [Inference-Time Scaling](../concepts/inference-time-scaling.md)
- [Long-Context Reasoning](../concepts/long-context-reasoning.md)
- [OOLONG Benchmark](../entities/oolong-benchmark.md)
- [BrowseComp-Plus](../entities/browsecomp-plus.md)
- [Recursive Language Models](../sources/2025-recursive-language-models.md)

## 来源

- [Recursive Language Models](../sources/2025-recursive-language-models.md)
