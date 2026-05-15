---
domain: wiki-maintenance
---

# Wiki 索引

这是整个 wiki 的主目录。浏览内容或回答问题时，优先先读这份索引。

## 元信息

- [全局概览](meta/overview.md) - 说明本 wiki 的范围、运行假设与当前状态。
- [Obsidian 首页](meta/obsidian-home.md) - 适合在 Obsidian 中日常浏览的导航页。

## 来源页面

- [Recursive Language Models](sources/2025-recursive-language-models.md) - 关于 RLM 的博客摘要，涵盖方法、实验、局限与未来方向。
- [工程技术：在智能体优先的世界中利用 Codex](sources/2026-harness-engineering-with-codex.md) - 关于 agent-first 软件工程、仓库知识设计与 Codex harness 的经验总结。
- [使用 Claude Code：HTML 的不可思议的有效性](sources/using-claude-code-html-effectiveness.md) - 关于为何在 Claude Code 工作流中用 HTML 取代长 Markdown 作为计划、评审、报告与交互式工件的倡议。
- [EWD 667: On the foolishness of "natural language programming"](sources/dijkstra-natural-language-programming.md) - Dijkstra 对自然语言编程构想的尖锐批判，以及他对形式符号系统与窄界面的坚持。
- [Evolution of HTTP](sources/evolution-of-http.md) - MDN 官方指南，覆盖 HTTP 从 0.9 到 3 的版本演进、安全层、REST 及协议扩展生态。

## 实体页面

- [OOLONG Benchmark](entities/oolong-benchmark.md) - 用于评估长上下文推理与聚合能力的重要基准。
- [BrowseComp-Plus](entities/browsecomp-plus.md) - 用于评估大规模文档集合上的多跳研究型问答基准。
- [Claude Code](entities/claude-code.md) - 在当前 wiki 中作为生成 HTML 工件、整合多源上下文并支撑人类审阅的编码代理环境。
- [Codex](entities/codex.md) - 在当前 wiki 中作为主要编码智能体与 agent-first 工程实践的核心实体。
- [Edsger W. Dijkstra](entities/edsger-dijkstra.md) - 荷兰计算机科学家，形式方法、结构化编程与并发理论先驱，对自然语言编程持激烈批判立场。
- [Tim Berners-Lee](entities/tim-berners-lee.md) - World Wide Web、HTTP 协议与 HTML 的创造者，CERN 时期的超文本系统设计师。

## 概念页面

- [Recursive Language Models](concepts/recursive-language-models.md) - 通过环境与递归子调用处理超长上下文的推理框架。
- [Context Rot](concepts/context-rot.md) - 上下文变长时模型理解、检索与推理能力退化的现象。
- [Inference-Time Scaling](concepts/inference-time-scaling.md) - 通过增加推理阶段计算与结构来提升效果的思路。
- [Long-Context Reasoning](concepts/long-context-reasoning.md) - 在超长输入上做检索、聚合、多跳推理与长输出生成的能力。
- [Agent-First Engineering](concepts/agent-first-engineering.md) - 将工程重心转向环境设计、约束编码与反馈回路的智能体优先开发方式。
- [HTML Artifacts](concepts/html-artifacts.md) - 由智能体生成、供人类直接浏览和操作的独立 HTML 工件，用于计划、评审、报告、原型与一次性编辑界面。
- [Natural Language Programming](concepts/natural-language-programming.md) - 用自然语言指示计算机执行任务的构想，从 Dijkstra 的批判到 LLM 时代 prompt 编程的新张力。
- [HTTP 协议演化](concepts/http.md) - HTTP 从单行协议到 QUIC 的版本演进，涵盖队头阻塞、可扩展性、安全层与 REST 等核心设计取舍。

## 分析页面

- [RLM、ReAct 与 RAG 的对比](analyses/rlm-vs-react-vs-rag.md) - 对三类长上下文与知识处理范式的适用场景、优劣势与不确定性进行对比。
- [RLM、总结式上下文管理与记忆系统的对比](analyses/rlm-vs-summarization-vs-memory-systems.md) - 对三类上下文管理路径的时间尺度、信息损失风险与适用问题进行对比。

## 维护说明

- 每个值得长期保留的页面都应在这里登记，并附上一行简介。
- 随着 wiki 增长，保持分类清晰、命名稳定。
- 如果已有相近条目，优先更新原条目，避免重复登记。
