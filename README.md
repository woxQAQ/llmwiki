# llm-wiki

一个用于搭建“由 LLM 持续维护的持久化知识 wiki”的起步骨架。

## 目录结构

- `raw/` - 用户收集的原始资料，只作为输入使用
- `wiki/` - 由 LLM 维护的 markdown 知识页面
- `AGENTS.md` - 约束 LLM 工作方式的 schema
- `templates/` - 供 LLM 生成页面时参考的模板
- `.obsidian/` - 面向 Obsidian 的基础配置

## 建议工作流

1. 把新资料放进 `raw/`。
2. 让你的 LLM agent 执行 ingest。
3. Agent 读取 `AGENTS.md`，更新 `wiki/` 下的页面，并向 `wiki/log.md` 追加日志。
4. 在 Obsidian 或任意 markdown 编辑器中浏览结果。

## 初始 wiki 布局

- `wiki/index.md` - wiki 页面总索引
- `wiki/log.md` - 追加式操作日志
- `wiki/meta/overview.md` - 全局概览与范围说明
- `wiki/meta/obsidian-home.md` - 适合作为 Obsidian 首页的导航页
- `wiki/sources/` - 每个来源的摘要与笔记
- `wiki/entities/` - 人物、组织、地点、工具等实体页
- `wiki/concepts/` - 概念、主题、方法、主张等概念页
- `wiki/analyses/` - 查询产物、比较、备忘录、报告等分析页

## Obsidian 友好配置

- 已设置附件目录为 `raw/assets/`
- 已设置模板目录为 `templates/`
- 已启用适合知识库维护的核心插件，如反向链接、出链、图谱、模板、标签面板等
- 可直接把仓库当作 Obsidian vault 打开使用

## 说明

- `raw/` 中的原始资料不应被 LLM 修改。
- `wiki/` 中的页面应随着资料与问题的积累持续演化。
- `AGENTS.md` 不是固定不变的，你可以和 agent 一起不断优化它。
