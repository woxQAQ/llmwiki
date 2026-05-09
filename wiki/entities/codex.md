---
title: Codex
type: entity
status: active
created: 2026-05-10
updated: 2026-05-10
domain: agentic-software-engineering
tags:
  - wiki/entity
  - llm/coding
  - llm/agents
source_files:
  - raw/assets/工程技术：在智能体优先的世界中利用 Codex.md
---

# Codex

## 摘要

- Codex 在当前 wiki 中指向 OpenAI 的编码智能体与相关工具链, 包括文中反复提到的 `Codex CLI` 与能直接在代码仓库中执行任务的智能体运行方式。
- 在这篇来源里, Codex 不是简单的代码补全工具, 而是软件交付流程中的主要执行者: 写代码、写测试、写文档、开 PR、处理审查反馈并合并变更。

## 关键要点

- Codex 的效果高度依赖仓库内是否存在可读的架构地图、规范、计划、工具和反馈回路。
- 作者把 Codex 的最佳使用方式描述为人类掌舵、智能体执行, 即人类负责目标、约束和判断, 智能体负责实现与迭代。
- Codex 在该案例中直接使用 `gh`、本地脚本、浏览器调试能力和可观测性查询, 说明其价值来自与工程环境的深度耦合, 不只是模型本身。
- 文中也强调, 如果仓库知识散落在聊天、Google Docs 或人脑中, 对 Codex 来说等于不存在。

## 证据与例子

- 首次提交到空仓库的初始结构由 `Codex CLI` 在模板指导下生成。
- 团队描述单次 Codex 运行可在单个任务上持续工作超过六小时。
- 文中列出的端到端能力包括复现缺陷、录制视频、实施修复、验证、开 PR、回应反馈和合并更改。

## 相关页面

- [Agent-First Engineering](../concepts/agent-first-engineering.md)
- [工程技术：在智能体优先的世界中利用 Codex](../sources/2026-harness-engineering-with-codex.md)

## 来源

- [工程技术：在智能体优先的世界中利用 Codex](../sources/2026-harness-engineering-with-codex.md)
