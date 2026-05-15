---
title: Claude Code
type: entity
status: active
created: 2026-05-12
updated: 2026-05-12
domain: agentic-software-engineering
tags:
  - wiki/entity
  - product
  - llm/coding
  - llm/agents
source_files:
  - raw/assets/Using Claude Code The Unreasonable Effectiveness of HTML使用 Claude 代码：HTML 的不可思议的有效性.md
---

# Claude Code

## 摘要

- 在当前 wiki 中，Claude Code 指向围绕 Claude 构建的编码代理工作环境；在本来源里，它不仅负责写代码，还负责生成供人类审阅的 HTML 工件，如计划、PR 解释、研究报告和一次性编辑界面。
- 这篇来源把 Claude Code 描绘成一种“上下文摄取器 + artifact 生成器”：先从文件系统、git 历史、浏览器和 MCP 数据源中读取材料，再把复杂信息压缩为更容易消费的 HTML 页面。
- 与把 agent 当作纯实现器不同，这里的 Claude Code 还承担了可视化解释器和交互式 UI 搭建器的角色。

## 关键要点

- Claude Code 可被直接提示去“做一个 HTML 文件”或“做一个 HTML artifact”，无需复杂技能封装即可开始使用。
- 在作者的工作流中，Claude Code 生成的 HTML 工件覆盖规划、代码评审、设计原型、研究总结和配置编辑等多种场景。
- 其优势来自上下文整合能力：除代码库外，文中还提到可以接入 MCP 数据源、浏览器状态和 git 历史。
- 作者特别强调，Claude Code 生成的 HTML 能帮助人类重新读完本来可能被忽略的长计划与复杂说明，从而保持人在回路中。

## 证据与例子

- 作者说 Claude Code 团队内部越来越多人把 HTML 当作默认输出格式，而不是 Markdown。
- 文中给出的示例 prompt 包括生成多方案 onboarding 设计对比、带严重级别标注的 PR 评审页面、可调动画参数的交互原型，以及带“复制为 markdown/JSON/diff”导出按钮的定制编辑器。
- 在验证阶段，作者还会让 verification agent 一并读取这些 HTML 文件，以保留更丰富的任务上下文。

## 张力或限制

- 作者承认 HTML 输出通常比 Markdown 慢 2 到 4 倍，并且在版本控制中更难审阅。
- 当前来源主要是产品内部倡议式经验总结，并未系统比较 Claude Code 与其他编码代理在 artifact 工作流上的差异。

## 相关页面

- [HTML Artifacts](../concepts/html-artifacts.md)
- [Agent-First Engineering](../concepts/agent-first-engineering.md)
- [使用 Claude Code：HTML 的不可思议的有效性](../sources/using-claude-code-html-effectiveness.md)

## 来源

- [使用 Claude Code：HTML 的不可思议的有效性](../sources/using-claude-code-html-effectiveness.md)
