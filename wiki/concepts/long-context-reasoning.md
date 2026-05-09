---
title: Long-Context Reasoning
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

# Long-Context Reasoning

## 摘要

- Long-context reasoning 关注模型在超长输入上进行检索、聚合、计数、多跳关联和长输出生成的能力。
- 本资料把问题重点从“上下文能否装下”转向“模型如何有效理解与利用超长上下文”。

## 关键要点

- 只看上下文窗口大小会误导判断, 因为很多失败并非来自截断, 而是来自理解与聚合能力下降。
- 需要把长上下文看成一个待操作的数据对象, 而不是一次性喂给模型的静态文本块。
- 在这一视角下, REPL、代码执行、递归子调用与总结都成为上下文处理工具。

## 证据与例子

- OOLONG 代表在单个超长上下文中做细粒度语义聚合与计数。
- BrowseComp-Plus 代表在巨大文档集合中做多跳查找与证据关联。
- LoCoDiff 被用来说明长输入加长输出的程序化任务同样适合 RLM 风格处理。

## 张力或争议

- 不同 benchmark 对 long-context reasoning 的定义差异很大。
- 某些任务更像检索问题, 某些更像程序执行问题, 很难用单一指标概括。

## 相关页面

- [Recursive Language Models](recursive-language-models.md)
- [Context Rot](context-rot.md)
- [OOLONG Benchmark](../entities/oolong-benchmark.md)
- [BrowseComp-Plus](../entities/browsecomp-plus.md)

## 来源

- [Recursive Language Models](../sources/2025-recursive-language-models.md)
