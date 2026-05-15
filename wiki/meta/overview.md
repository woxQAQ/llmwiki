---
domain: wiki-maintenance
---

# 全局概览

## 目的

这个 wiki 用来把原始资料持续沉淀为由 LLM agent 维护的持久化 markdown 知识库。

## 当前状态

- 这个 wiki 已经完成初始化，并持续 ingest 与 LLM 工程实践相关的来源资料。
- 当前的内容簇主要围绕三条主线展开: 长上下文推理与递归语言模型 scaffold, agent-first 软件工程与 Codex harness 设计, 以及面向人类审阅的 HTML artifact 工作流。
- `wiki/index.md` 是主导航文件。
- `wiki/meta/obsidian-home.md` 是适合在 Obsidian 中使用的首页导航页。
- `wiki/log.md` 用于记录 ingest、query 与维护操作的时间线。

## 预期知识流

1. 将整理好的来源资料放入 `raw/`。
2. 逐篇或按小批量执行 ingest。
3. 更新可长期复用的概念页与实体页。
4. 将有长期价值的分析结果保存回 wiki。
5. 定期执行 lint，检查缺口、冲突、孤立页面与过时内容。

## 建议的下一步

- 增加更多与长上下文推理、agent、retrieval、memory 或 coding agents 相关的论文与博客。
- 如果作者、实验室、模型、产品或 benchmark 家族反复出现，就为它们扩展独立实体页。
- 增加更多分析页面，例如比较 agent-first engineering 与传统工程流程、Copilot 式协作或自主软件工程系统。
- 增加更多关于 agent-generated interfaces、artifact workflows 与 human-in-the-loop review surfaces 的来源与案例。
